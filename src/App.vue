<template>
  <el-header role="banner"> header </el-header>
  <el-main>
    <!-- Opening is dialog causes an accessibility issue - "Document should not have more than one banner landmark -->
    <el-button text @click="dialogVisible = true">
      click to open the Dialog
    </el-button>
    <el-dialog v-model="dialogVisible" title="Tips" width="30%" append-to-body>
      <span>text</span>
    </el-dialog>

    <!-- Opening a filter dropdown in the table causes an accessibility issue - "All page content should be contained by landmarks" -->
    <TableEx />

    <!-- Opening a sizes dropdown causes an accessibility issue - "All page content should be contained by landmarks" -->
    <el-pagination layout="sizes, prev, pager, next" :total="50" />
  </el-main>
</template>

<script>
import TableEx from "./components/TableEx.vue";
export default {
  components: {
    TableEx,
  },

  data() {
    return {
      dialogVisible: false,
    };
  },
};
</script>
