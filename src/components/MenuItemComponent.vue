<template>
  <div
    class=" h-screen w-full border-slate-200 border-y-2 rounded-md "
    v-for="(main,index) in menu"
    :key="index"
    :class="{'background-dark': index%2==0 , 'background-white' : index%2 !=0}"
  >
    <div class="items-center mx-auto py-10 px-8 " :id="main.name" >
      <h2 class="pt-5 text-4xl font-bold text-center lobster">{{ main.name }}</h2>
      <img
        class="self-center rounded-md h-auto w-full lg:max-w-sm my-5 mx-0 shadow-lg  shadow-black max-w-full"
        :src="main.image"
        alt="Fotoğraf"
      />
      <div
        class="flex flex-col my-5 mx-0 w-full"
        v-for="(item, pindex) in main.menus"
        :key="pindex"
        
      >
        <div class="flex text-base justify-between border-b " :class="{'border-black': index%2!=0 , 'border-white' : index%2 ==0}" >
          <p class="m-0 font-bold">{{ item.name }}</p>
          <p class="m-0">{{ item.price }} &#x20BA; </p>
        </div>
        <p class="">{{item.description}}</p>

     
      </div>
    </div>

    
  </div>
</template>

<script>

export default {
  props: ["menu"],
  data() {
    return {
        bgwhite: "bg-white",

    }
  },
  name: "menu-item",
  
  
  
};
</script>

<style scoped>
.background-dark{
    background-color: #333;
    color: #f1f1f1;
}
.background-white{
    background-color: #f1f1f1;
    color: #333;
}




</style>