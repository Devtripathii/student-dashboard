<template>
  <div class="profile">
    <h2>Student Profile</h2>
    <p><strong>Name:</strong> {{ student.name }}</p>
    <p><strong>ID:</strong> {{ student.id }}</p>
    <p><strong>Email:</strong> {{ student.email }}</p>
  </div>
</template>

<script>
export default {
  name: "StudentProfile",
  props: {
    student: Object,
  },
};
</script>

<style scoped>
.profile {
  border: 1px solid #ddd;
  padding: 15px;
  border-radius: 8px;
}
</style>
