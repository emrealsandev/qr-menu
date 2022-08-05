<template>
  <div >
    <menu-item-component 
    v-for="(item,index) in menu"
    :key="index"
    :label="item.label"
    :image="item.image"
    :data="item.children"
    />
  </div>
</template>

<script>
import MenuItemComponent from "./MenuItemComponent.vue";
export default {
  components: {
    MenuItemComponent,
  },
  data() {
    return {
      menu: [
        {
          label: "Kahvaltı",
          image: "kahvalti",
          children: [
            {
              label: "Yumurta",
              price: 35,
              desc: "Sağında veya solunda yumurta",
            },
            {
              label: "Sucuk",
              price: 90,
              desc: "Uludağ Sucuk Ekmek",
            },
            {
              label: "Kuymak",
              price: 40,
              desc: "Kolot peynirli kuymak",
            },
            {
              label: "Salçalı Sosis",
              price: 20,
              desc: "Domuz Eti Değildir",
            },
          ],
        },
        {
          label: "Çorba",
          image: "corba",
          children: [
            {
                label: "Mercimek",
                price: 35,
                desc: "Sağında veya solunda yumurta",
              },
              {
                label: "Sucuk",
                price: 90,
                desc: "Uludağ Sucuk Ekmek",
              },
              {
                label: "Kuymak",
                price: 40,
                desc: "Kolot peynirli kuymak",
              },
              {
                label: "Salçalı Sosis",
                price: 20,
                desc: "Domuz Eti Değildir",
              },
          ],
          
        },
        
      ],
    };
  },
};
</script>
