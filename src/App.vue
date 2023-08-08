<template>
  <el-header role="banner"> header </el-header>
  <el-main>
    <el-button text @click="dialogVisible = true">
      click to open the Dialog
    </el-button>
    <el-dialog v-model="dialogVisible" title="Tips" width="30%" append-to-body>
      <span>This is a message</span>
    </el-dialog>
  </el-main>
</template>

<script>
export default {
  data() {
    return {
      dialogVisible: false,
    };
  },
};
</script>
