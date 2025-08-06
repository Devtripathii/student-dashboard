<template>
  <div class="notifications">
    <h2>Notifications</h2>
    <ul>
      <li v-for="(note, index) in notifications" :key="index">{{ note }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "Notifications",
  props: {
    notifications: Array,
  },
};
</script>

<style scoped>
.notifications ul {
  list-style: disc;
  padding-left: 20px;
}
</style>
