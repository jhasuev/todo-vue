<template>
  <div :class="['item', { ready }]" ref="item">
    <Checkbox class="item__checkbox" />
    <div class="item__text">Lorem ipsum dolor, sit amet consectetur adipisicing elit. Cum, a.</div>
    <Btn class="item__btn" />
    
    <div :style="{height: `${maxHeight}px`}" />
  </div>
</template>

<script>
  import Checkbox from "./checkbox"
  import Btn from "./btn"
  export default {
    name: 'TodoListItem',
    components: {
      Checkbox,
      Btn,
    },
    data() {
      return {
        ready: false,
        maxHeight: 0,
      }
    },
    mounted() {
      this.$refs.item.children.forEach(child => {
        this.maxHeight = Math.max(this.maxHeight, parseFloat(getComputedStyle(child).height))
      })

      this.ready = true
    }
  }
</script>

<style lang="scss" scoped>

  .item {
    display: flex;
    align-items: center;
    padding: 5px 0;

    &__checkbox {
      margin-right: 10px;
    }

    &__text {
      white-space: nowrap;
      text-overflow: ellipsis;
      overflow: hidden;
      margin-right: 10px;
      font-size: 18px;
    }

    &.ready &__btn {
      display: none;
    }

    &.ready:hover &__btn {
      display: block;
    }
  }

</style>