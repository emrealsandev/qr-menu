<template>
  <div  class="max-w-5xl mx-auto py-5">
    <header
      class="items-center bg-neutral-700 text-white flex h-10 left-0 py-0 px-5 fixed top-0 w-full"
    >
      Menu
    </header>
    <div
      class="welcoming items-center h-screen justify-center w-full flex flex-col"
    >
      <img class="w-full my-0 mx-auto p-0 h-auto max-w-lg" src="./assets/logo.png" alt="" />

      <div class="welcoming-message items-center flex flex-col justify-center">
        <h1 class="font-mono font-bold text-4xl">Hoş Geldiniz</h1>
      </div>
        </div>
      <div class="category-container">
        <menu-component></menu-component>
      </div>
  </div>
</template>

<script>
import MenuComponent from "./components/MenuComponent.vue";
export default {
  name: "App",
  components: {
    MenuComponent,
  },
};
</script>

<style>
* {
  padding: 0;
  margin: 0;
  box-sizing: content-box;
}
</style>
