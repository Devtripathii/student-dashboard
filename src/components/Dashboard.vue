<template>
  <div class="dashboard">
    <StudentProfile :student="student" />
    <CourseProgress :courses="courses" />
    <AssignmentsList :assignments="assignments" />
    <Notifications :notifications="notifications" />
  </div>
</template>

<script>
import StudentProfile from "./StudentProfile.vue";
import CourseProgress from "./CourseProgress.vue";
import AssignmentsList from "./AssignmentsList.vue";
import Notifications from "./Notifications.vue";

export default {
  name: "Dashboard",
  components: {
    StudentProfile,
    CourseProgress,
    AssignmentsList,
    Notifications,
  },
  data() {
    return {
      student: {
        name: "John Doe",
        id: "S12345",
        email: "john.doe@example.com",
      },
      courses: [
        { name: "Math 101", progress: 75 },
        { name: "Physics 201", progress: 40 },
        { name: "History 301", progress: 90 },
      ],
      assignments: [
        { title: "Math Homework 1", dueDate: "2025-08-01", status: "pending" },
        { title: "Physics Lab Report", dueDate: "2025-08-10", status: "done" },
      ],
      notifications: [
        "Exam scheduled on August 15.",
        "Library will be closed on August 5.",
      ],
    };
  },
};
</script>

<style scoped>
.dashboard {
  max-width: 600px;
  margin: 40px auto;
  font-family: Arial, sans-serif;
  display: grid;
  grid-gap: 20px;
}
</style>
