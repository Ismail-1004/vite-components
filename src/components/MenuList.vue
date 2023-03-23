<template>
  <ul class="list">
    <li class="list__item icon">
      <router-link to=""> <i class="fa-sharp fa-solid fa-chart-simple"></i> </router-link>
    </li>
    <li class="list__item icon">
      <router-link to=""> <i class="fa-solid fa-user"></i> </router-link>
    </li>
    <li class="list__item danger icon">
      <i class="fa-solid fa-right-from-bracket"></i>
    </li>
  </ul>
</template>

<style lang="scss" scoped>
.list {
  display: flex;
  align-items: center;
  list-style: none;
  padding-left: 0;

  &__item {
    &:not(:last-child) {
      margin-right: 20px;
    }
  }

  & .icon {
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
</style>