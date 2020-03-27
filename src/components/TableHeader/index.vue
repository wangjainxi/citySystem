<template>
  <div class="table-header">
    <h3>
      <slot />
    </h3>
    <span />
    <div class="table-header-btn">
      <el-button class="filter-item" style="margin-left: 10px;" type="primary" @click="addEvent">添加</el-button>
      <el-button class="filter-item" style="margin-left: 10px;" type="primary" @click="deleteEvent">删除</el-button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'TableHeader',
  methods: {
    addEvent() {
      this.$emit('addEvent')
    },
    deleteEvent() {
      this.$emit('deleteEvent')
    }
  }
}
</script>

<style lang="scss">
.table-header {
  display: flex;
  align-items: center;
  height: 46px;
  padding: 0 10px;
  border-radius: 8px;
  margin-top: 10px;
  background-color: #bdddff;
  span {
    flex: 1;
  }
  &-btn {
    padding-right: 20px;
  }
}
</style>
