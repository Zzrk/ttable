  <template>
  <div class="ttable">
    <el-table :data="data" style="width: 100%">
      <el-table-column type="index" label="编号" width="180"> </el-table-column>
      <slot></slot>
    </el-table>
    <el-pagination background layout="prev, pager, next" :total="100" @current-change="pageChange" ref="pagination">
    </el-pagination>
  </div>
</template>

<script>
export default {
  props: {
    data: Array,
  },
  data() {
    return {};
  },
  methods:{
    pageChange(){
      console.log(this.$refs.pagination,this.$refs.pagination.currentPage)
    }
  },
};
</script>

<style>
</style>