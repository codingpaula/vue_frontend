<template>
  <div class="home">
    <MatrixMain />
  </div>
</template>

<script>
// @ is an alias to /src
import MatrixMain from "@/components/MatrixMain.vue";

export default {
  name: "home",
  components: {
    MatrixMain
  }
};
</script>

<style scoped>
.home {
  padding: 1rem;
  background-color: #f2ece1;
  height: 100%;
}
</style>
