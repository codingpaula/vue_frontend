<template lang="html">
  <div id="task">
    {{ task.name }}
  </div>
</template>

<script>
export default {
  name: "Task",
  props: [
    "task",
    // "colors"
  ]
}
</script>

<style lang="css">
</style>
