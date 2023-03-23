<template>
  <div>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.3.0/css/all.min.css"
      integrity="sha512-SzlrxWUlpfuzQ+pcUCosxcglQRNAq/DZjVsC0lE40xsADsfeQoEypE+enwcOiGjk/bSuGGKHEyjSoQ1zVisanQ=="
      crossorigin="anonymous" referrerpolicy="no-referrer" />

    <Menu :logo="false">
      <template v-slot:primary>
        <Flex>
          <MenuButton>
            <template v-slot:title> Menu </template>
          </MenuButton>

          <MenuButton>
            <template v-slot:title> More Apps </template>
          </MenuButton>
        </Flex>
      </template>

      <template v-slot:secondary>
        <MenuList />
      </template>
    </Menu>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

import Menu from '@/components/Menu.vue';
import MenuButton from '@/components/MenuButton.vue';
import MenuList from '@/components/MenuList.vue'
import Flex from '@/components/Flex.vue'

export default defineComponent({
  name: 'App',
  components: {
    Menu,
    MenuButton,
    MenuList,
    Flex
  }
})
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
</style>
