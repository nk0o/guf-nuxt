<template>
  <button :class="['btn', variant]" @click="handleClick">
    <slot />
  </button>
</template>

<script>
export default {
  name: "Button",
  props: {
    variant: {
      type: String,
      default: "primary", // 기본 스타일: primary
    },
  },
  methods: {
    handleClick() {
      this.$emit("click");
    },
  },
};
</script>

<style scoped>
.btn {
  padding: 10px 20px;
  border: none;
  border-radius: 4px;
  font-size: 16px;
  cursor: pointer;
}
.btn.primary {
  background-color: #007bff;
  color: white;
}
.btn.secondary {
  background-color: #6c757d;
  color: white;
}
.btn.success {
  background-color: #28a745;
  color: white;
}
</style>
