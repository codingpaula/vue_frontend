<template lang="html">
  <div id="topic-side">
    <h3>My Topics</h3>
    <div v-for="topic in topics">
      <Topic v-bind:topic="topic" />
    </div>
    <b-button class="toggle">
      toggle all
    </b-button>
  </div>
</template>

<script>
import Topic from "@/components/Matrix/Topic.vue";

export default {
  name: "TopicSide",
  components: {
    Topic
  },
  props: ["topics"]
}
</script>

<style lang="css" scoped>
#topic-side {
  background-color: #ece2d1;
  padding: 0.5rem;
}
h3 {
  border-bottom: 1px solid #444444;
}
.toggle {
  margin-top: 1rem;
  width: 100%;
}
</style>
