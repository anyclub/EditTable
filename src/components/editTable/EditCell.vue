<template>
  <div class="editCell" @dblclick="changeDisabled">
    {{ showValue }}
  </div>
</template>

<script>
export default {
  name: "EditCell",
  props: {
    data: {
      type: Object
    }
  },
  computed: {
    showValue() {
      let key = this.data.column.property;
      return this.data.row[key];
    }
  },
  methods: {
    changeDisabled() {
      console.log(this.data);
    }
  },
  created() {
    this.$on("changeDisabled", function() {
      console.log("on");
    });
  }
};
</script>


<style lang="less" scoped>
.editCell {
  padding: 12px 11px;
}
</style>
