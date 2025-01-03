<template>
  <div class="components-page">
    <h1>Components Collection</h1>
    <section class="component-section">
      <h2>Button Component</h2>
      <Button variant="primary" @click="handleClick">Primary Button</Button>
      <Button variant="secondary" @click="handleClick">Secondary Button</Button>
      <Button variant="success" @click="handleClick">Success Button</Button>
    </section>
  </div>
</template>

<script>
import Button from "~/components/Button.vue";

export default {
  components: {
    Button,
  },
  methods: {
    handleClick() {
      alert("Button clicked!");
    },
  },
};
</script>

<style scoped>
.components-page {
  padding: 20px;
}
.component-section {
  margin-bottom: 40px;
}
h2 {
  margin-bottom: 20px;
}
</style>
