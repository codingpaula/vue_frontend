<template lang="html">
  <b-button-group class="topic-btn">
    <b-button class="topic-btn-edit" :style="bgColors">
      i
    </b-button>
    <b-button class="topic-btn-middle":style="bgColors">
      {{topic.name}}
    </b-button>
    <b-button class="topic-btn-plus" :style="bgColors">
      +
    </b-button>
  </b-button-group>
</template>

<script>
export default {
  name: "Topic",
  props: ["topic"],
  computed: {
    bgColors: function() {
      return {
        '--color': '#' + this.topic.color,
        '--color-hover': '#' + this.topic.hover,
        '--color-border': '#' + this.topic.border
      }
    }
  }
}
</script>

<style lang="css" scoped>
button {
  background-color: var(--color);
  border: 1px solid var(--color);
}
button:hover {
  background-color: var(--color-hover);
  border: 1px solid var(--color-hover);
}
.topic-btn {
  width: 100%;
  padding-top: 0.25rem;
  padding-bottom: 0.25rem;
}
.topic-btn-middle {
  border-left: 1px solid var(--color-hover);
  border-right: 1px solid var(--color-hover);
}
.topic-btn-edit,
.topic-btn-plus {
  max-width: 50px;
}
.topic-btn-edit {
  border-right: 1px solid var(--color-hover);
}
.topic-btn-plus {
  border-left: 1px solid var(--color-hover);
}
</style>
