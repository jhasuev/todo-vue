<template>
  <button class="btn  btn--blue">
    Add
  </button>
</template>

<script>
  export default {
    name: 'Btn',
  }
</script>

<style lang="scss" scoped>
  .btn {
    position: relative;
    z-index: 1;
    display: inline-block;
    padding: 10px;

    cursor: pointer;
    background-color: #333;
    color: #fff;

    &:after {
      content: "";
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      bottom: 0;
      background-color: #fff;
      z-index: -1;
      opacity: 0;
      transition: opacity .2s;
    }

    &:hover:after {
      opacity: 0.3;
    }

    &:focus:after {
      opacity: 0.2;
    }

    &--blue {
      background-color: #097fce;
    }
  }
</style>