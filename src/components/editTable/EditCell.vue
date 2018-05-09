<template>
  <div class="editCell" @dblclick="changeDisabled" ref="cell">
    <div v-if="!editting" class="text-wrap">
      {{ value | showValue(type, selectOptions, selectConfig)}}
    </div>
    <template v-else>
      <el-select v-if="type=='select'" v-model="value" ref="input" automatic-dropdown @visible-change="visibleChange">
        <el-option v-for="itm in selectOptions" :key="itm[selectConfig.value]" :value="itm[selectConfig.value]" :label="itm[selectConfig.label]"></el-option>
      </el-select>
      <el-select v-if="type=='selectRemote'" v-model="value" ref="input" @visible-change="visibleChange" :remote-method="keyWord=>searchKeyWord(keyWord,item.dataKey,item.url)" :loading="selectLoading" filterable remote>
        <el-option v-for="itm in selectOptions" :key="itm.code" :value="itm.code" :label="itm.name"></el-option>
      </el-select>
      <el-input v-if="type=='input'" v-model="value" ref="input" @blur="blurEdit" @keypress.enter.native="$event.target.blur()">
      </el-input>
    </template>
  </div>
</template>

<script>
export default {
  name: "EditCell",
  props: {
    data: Object,
    type: {
      default: "input",
      type: String
    },
    selectConfig: {
      type: Object,
      default: () => {
        return {
          label: "name",
          value: "code"
        };
      }
    },
    selectOptions: {
      type: Array,
      default: () => {
        return [];
      }
    },
    url: String,
    correlation: String
  },
  filters: {
    showValue(value, type, selectOptions, selectConfig) {
      if (type !== "input") {
        for (let i = 0; i < selectOptions.length; i++) {
          if (selectOptions[i][selectConfig.value] == value) {
            return selectOptions[i][selectConfig.label];
          }
        }
      }
      return value;
    }
  },
  data() {
    return {
      editting: false,
      value: this.data.row[this.data.column.property],
      productSelect: [],
      selectLoading: false
    };
  },
  computed: {
    showValue() {
      let key = this.data.column.property;
      return this.data.row[this.data.column.property];
    }
  },
  methods: {
    test() {
      console.log("test");
    },
    changeDisabled() {
      this.editting = true;
      this.$nextTick(() => {
        if (this.type == "selectRemote") {
        }
        this.$refs.input.focus();
      });
    },
    blurEdit() {
      this.editting = false;
      this.changeValue();
    },
    visibleChange(flag) {
      if (!flag) {
        this.blurEdit();
      }
    },
    changeValue() {
      this.$emit("changeValue", this.value, this.data.$index, this.data.column.property);
    },
    searchKeyWord(key) {
      this.selectLoading = true;
      // const { data } = await this.getRequest(`${url}/${key}`);
      this.selectLoading = false;
    }
  }
};
</script>


<style lang="less" scoped>
.editCell {
  width: 100%;
  height: 40px;
  line-height: 16px;
  .text-wrap {
    padding: 12px 11px;
    white-space: nowrap;
    text-overflow: ellipsis;
    overflow: hidden;
  }
  /deep/ .el-input__inner {
    padding: 11px 10px;
  }
}
</style>
