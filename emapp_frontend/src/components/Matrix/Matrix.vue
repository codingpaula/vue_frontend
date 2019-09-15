<template lang="html">
  <div id="matrix">
    <div v-for="task in tasks">
      <Task v-bind:task="task" />
    </div>
  </div>
</template>

<script>
import Task from '@/components/Matrix/Task.vue';

export default {
  name: "Matrix",
  components: {
    Task
  },
  props: [
    "topics",
    "tasks"
  ]
}
</script>

<style lang="css">
#matrix {
  background-color: #eeeeee;
}
</style>
