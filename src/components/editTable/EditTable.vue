<template>
  <el-table height="100%" @selection-change="selectionChange" :fit="true" :data="tableData" v-loading="loading" border stripe class="editTable" align="left">
    <el-table-column v-if="checked" class-name="checkRow" type="selection" fixed="left">
    </el-table-column>
    <el-table-column v-if="index" class-name="indexRow" type="index" :index="1">
    </el-table-column>
    <el-table-column v-for="item in tableIndex " :key="item.dataKey " :prop="item.dataKey " :label="item.name " :width="item.width">
      <template slot-scope="scope">
        <EditCell :type="item.type" :data="scope" :url="item.url" :correlation="item.correlation" :selectOptions="item.selectOptions" @changeValue="changeValue"></EditCell>
      </template>
    </el-table-column>
  </el-table>
</template>

<script>
import EditCell from "./EditCell";
export default {
  name: "editTable",
  components: {
    EditCell
  },
  props: {
    defaultData: {
      type: Array
    },
    tableIndex: {
      type: Array,
      required: true
    },
    checked: {
      type: Boolean,
      default: true
    },
    index: {
      type: Boolean,
      default: true
    }
  },
  data() {
    return {
      loading: false,
      tableData: []
    };
  },
  watch: {
    defaultData: {
      handler: function(val) {
        this.tableData = val;
      },
      immediate: true
    }
  },
  methods: {
    selectionChange(val) {
      console.log(val);
    },
    changeValue(val, rowIndex, key) {
      // console.log(val);
      // console.log(rowIndex);
      // console.log(key);
      this.tableData[rowIndex][key] = val;
    }
  }
};
</script>

<style lang="less" scoped>
.editTable {
  /deep/ td,
  /deep/ .cell {
    padding: 0;
  }
}
</style>
