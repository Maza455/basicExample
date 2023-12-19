<template>
  <button @click="toggleLogo" class="my_button">
    <slot v-if="!showLogo"></slot>
    <img v-else src="../assets/logo.png" alt="Logo">
  </button>
</template>

<script>
export default {
  name: 'ButtonComp',
  data() {
    return {
      showLogo: false
    };
  },
  methods: {
    toggleLogo() {
      this.showLogo = !this.showLogo;
    }
  }
}
</script>

<style>
.my_button {
  font-size: 24px;
  padding: 16px 32px;
  background-color: indigo;
  color: white;
  border: none;
  border-radius: 8px;
  cursor: pointer;
  display: block;
  margin: 0 auto;
}
</style>