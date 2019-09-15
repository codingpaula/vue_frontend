<template>
  <b-container fluid class="main">
    <b-row>
      <b-col cols="3" class="topics">
        <TopicSide v-bind:topics="topics"/>
      </b-col>
      <b-col cols="7" class="matrix">
        <Matrix v-bind:topics="topics" v-bind:tasks="tasks"/>
      </b-col>
      <b-col cols="2" class="settings">
        <SettingSide />
      </b-col>
    </b-row>
  </b-container>
</template>

<script>
import Matrix from "@/components/Matrix/Matrix.vue";
import SettingSide from "@/components/Matrix/SettingSide.vue";
import TopicSide from "@/components/Matrix/TopicSide.vue";

export default {
  name: "MatrixMain",
  components: {
    Matrix,
    SettingSide,
    TopicSide
  },
  data() {
    return {
      topics: [
        {
          id: 1,
          name: "Topic 1",
          color: "30a64a",
          hover: "28883d",
          border: "1f6a30",
          selected: true
        },
        {
          id: 2,
          name: "Topic 2",
          color: "ff9300",
          hover: "d17900",
          border: "a35e00",
          selected: true
        },
        {
          id: 3,
          name: "Topic 3",
          color: "0096ff",
          hover: "007bd1",
          border: "0060a3",
          selected: true
        }
      ],
      tasks: [
        {
          id: 1,
          name: "Task 1",
          topic: 1,
          important: 65,
          done: false,
          description: "This is the description of Task 1.",
          duedate: ""
        },
        {
          id: 2,
          name: "Task 2",
          topic: 1,
          important: 23,
          done: false,
          description: "This is the description of Task 2.",
          duedate: ""
        },
        {
          id: 3,
          name: "Task 3",
          topic: 2,
          important: 90,
          done: false,
          description: "This is the description of Task 3.",
          duedate: ""
        },
        {
          id: 4,
          name: "Task 4",
          topic: 2,
          important: 12,
          done: false,
          description: "This is the description of Task 4.",
          duedate: ""
        },
        {
          id: 5,
          name: "Task 5",
          topic: 2,
          important: 50,
          done: false,
          description: "This is the description of Task 5.",
          duedate: ""
        },
        {
          id: 6,
          name: "Task 6",
          topic: 3,
          important: 100,
          done: false,
          description: "This is the description of Task 6.",
          duedate: ""
        },
        {
          id: 7,
          name: "Task 7",
          topic: 3,
          important: 80,
          done: false,
          description: "This is the description of Task 7.",
          duedate: ""
        }
      ]
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
.topics,
.matrix,
.settings {
  padding: 0;
}
</style>
