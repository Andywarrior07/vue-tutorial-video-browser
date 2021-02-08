<template>
  <div>
    <input type="text" placeholder="Search..." @input="onInput" />
  </div>
</template>

<script>
export default {
  name: 'SearchBar',
  methods: {
    onInput({ target }) {
      const { value } = target;

      this.$emit('termChange', value);
    },
  },
};
</script>

<style scoped>
input {
  width: 75%;
}

div {
  text-align: center;
  margin: 20px;
}
</style>
