<template>
  <teleport to="body">
    <div v-if="isVisible" class="notification-alert">
      {{ message }}
    </div>
  </teleport>
</template>

<script>
export default {
  name: "AlertNotification",
  props: {
    message: {
      type: String,
      default: "Notification message!",
    },
  },
  data() {
    return {
      isVisible: false,
    };
  },
  methods: {
    show() {
      this.isVisible = true;
      setTimeout(() => {
        this.isVisible = false;
      }, 3000);
    },
  },
};
</script>

<style scoped>
.notification-alert {
  position: fixed;
  top: 20px;
  right: 20px;
  background-color: #4caf50;
  color: white;
  padding: 15px;
  border-radius: 5px;
  box-shadow: 0px 4px 6px rgba(0, 0, 0, 0.1);
  z-index: 9999;
  transition: opacity 0.5s;
}
</style>
