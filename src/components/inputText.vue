<template>
  <input type="text" class="field" placeholder="Enter todo">
</template>

<script>
  export default {
    name: 'InputText',
  }
</script>

<style lang="scss" scoped>
  .field {
    border: 1px solid #eee;
    padding: 4px 10px;
    transition: box-shadow .2s;

    &:focus {
      box-shadow:0 0 5px rgba(0,0,0,.2)
    }
  }
</style>