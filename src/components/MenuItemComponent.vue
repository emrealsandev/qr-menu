<template>
  <div
    class=" h-screen w-full border-slate-200 border-y-2 rounded-md"
    v-for="(main,index) in menu"
    :key="index"
    :class="{'background-dark': index%2==0 , 'background-white' : index%2 !=0}"
  >
    <div class="items-center mx-auto py-10 px-8"  >
      <h2 class="pt-5 text-4xl font-bold text-center ">{{ main.label }}</h2>
      <img
        class="self-center rounded-md h-auto w-full my-5 mx-0 shadow-lg  shadow-black max-w-full"
        :src="require(`../assets/img/${main.image}.jpg`)"
        alt="Fotoğraf"
      />
      <div
        class="flex flex-col my-5 mx-0 w-full"
        v-for="(item, pindex) in main.children"
        :key="pindex"
        
      >
        <div class="flex text-base justify-between border-b" :class="{'border-black': index%2!=0 , 'border-white' : index%2 ==0}" >
          <p class="m-0">{{ item.label }}</p>
          <p class="m-0">{{ item.price }} TL</p>
        </div>
        <p class="mt-2">{{item.desc}}</p>

        <!-- <ul>
                    <li v-for="(item,index) in data" :key="index"><span style="float: left;"> {{item.label}}</span> : <span style="float:right;">{{item.price}} TL</span></li>
                    
                </ul> -->
      </div>
    </div>

    <!-- <div class="sub_category" >
    <div class="sub_category_name">{{ label }}</div>
    <div class="single-menu-item" v-for="(item, index) in data" :key="index">
      <div class="menu-item-header">
        <p class="menu-item-name">{{ item.label }}</p>
        <p class="menu-item-desc">{{ item.desc }}</p>
        <p>{{ item.price }}</p>
      </div>
    </div>
  </div> -->
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