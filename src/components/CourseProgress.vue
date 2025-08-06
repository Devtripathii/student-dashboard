<template>
  <div class="courses">
    <h2>Course Progress</h2>
    <ul>
      <li v-for="course in courses" :key="course.name">
        {{ course.name }} - {{ course.progress }}%
        <div class="progress-bar">
          <div class="progress" :style="{ width: course.progress + '%' }"></div>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "CourseProgress",
  props: {
    courses: Array,
  },
};
</script>

<style scoped>
.progress-bar {
  background: #eee;
  border-radius: 5px;
  overflow: hidden;
  height: 10px;
  margin-top: 5px;
}
.progress {
  background-color: #4caf50;
  height: 100%;
}
</style>
