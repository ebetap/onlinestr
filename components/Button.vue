<template>
  <button class="btn">
    {{ label }}
  </button>
</template>

<script>
export default {
  name: 'Button',
  props: {
    onClick: Function,
    label: String,
    type: String
  }
}
</script>

<style scoped>
.btn {
  background: #333;
  color: #ffffff;
  min-width: 150px;
  font-size: 1rem;
  cursor: pointer;
}
.btn:hover {
  background: #4f4f4f;
}
.btn:focus {
  outline: none;
}
</style>
