<template>
  <div class="assignments">
    <h2>Assignments</h2>
    <ul>
      <li v-for="assignment in assignments" :key="assignment.title">
        <span>{{ assignment.title }} - Due: {{ assignment.dueDate }}</span>
        <span :class="{ done: assignment.status === 'done' }">
          {{ assignment.status }}
        </span>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "AssignmentsList",
  props: {
    assignments: Array,
  },
};
</script>

<style scoped>
.done {
  color: green;
  font-weight: bold;
}
.assignments ul {
  list-style: none;
  padding-left: 0;
}
.assignments li {
  display: flex;
  justify-content: space-between;
  padding: 5px 0;
}
</style>
