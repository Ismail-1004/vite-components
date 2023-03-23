<template>
  <nav class="menu">
    <div class="menu__logo">
      <img src="" alt="logo" class="menu__logo-img" v-show="logo">
      <slot name="primary">
      </slot>
    </div>

    <slot name="secondary"></slot>
  </nav>
</template>

<script>
export default {
  props: {
    logo: {
      type: Boolean,
      required: false,
      default: false
    }
  }
}
</script>

<style lang="scss" scoped>
.menu {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 10px;
  box-shadow: 0 1px 0px rgba(0,0,0,0.25), 0 1px 1px rgba(0,0,0,0.22);

  &__logo {
    align-items: center;

    &-img {
      width: 50px;
      margin-right: 10px;
    }
  }

  & .standard {
    padding: 10px;
    display: inline-block;
    transition: .1s;
    border-radius: 5px;

    &__icon {
      border: 1px solid black;
      padding: 10px 15px;
      border-radius: 5px;
      cursor: pointer;
      font-size: 18px;

      &.danger {
        border: 1px solid red;
        color: red;
      }
    }
  }

  & .d-flex {
    display: flex;
  }
}
</style>