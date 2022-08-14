<template>
  <div >
    <menu-item-component 
    :menu = "menu"
    />
  </div>
</template>

<script>
import MenuItemComponent from "./MenuItemComponent.vue";
import axios from "axios";
export default {
  components: {
    MenuItemComponent,
  },
  data() {
    return {
      menu: [],
    };
  },
    created() {
    axios.get('http://127.0.0.1:8000/api/menu')
    .then((response) => {
      this.menu = response.data.data;

    });
  },

  
};
</script>

<style >

</style>