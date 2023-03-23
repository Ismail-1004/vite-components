<template>
  <button class="btn">
    <slot name="title"></slot>
  </button>
</template>

<style lang="scss" scoped>
.btn {
  padding: 10px;
  display: inline-block;
  transition: .1s;
  border-radius: 5px;
  font-family: sans-serif;

  border: none;
  background: none;

  &.danger {
    &:hover {
      background: red;
      color: white;
    }
  }

  &:hover {
    background: rgba(128, 128, 128, 0.667);
  }
}
</style>