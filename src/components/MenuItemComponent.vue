<template>
  <div
    class="bg-neutral-700 h-screen w-full border-slate-200 border-y-2 rounded-md"
  >
    <div class="items-center text-white mx-auto py-10 px-8">
      <h2 class="pt-5 text-4xl font-bold text-center">{{ label }}</h2>
      <img
        class="self-center rounded-md h-auto w-full my-5 mx-0 shadow-lg shadow-black max-w-full"
        :src="require(`../assets/img/${image}.jpg`)"
        alt="Fotoğraf"
      />
      <div
        class="flex flex-col my-5 mx-0 w-full"
        v-for="(item, index) in data"
        :key="index"
        
      >
        <div class="flex text-base justify-between border-b">
          <p class="m-0">{{ item.label }}</p>
          <p class="m-0">{{ item.price }} TL</p>
        </div>
        <p>{{item.desc}}</p>

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
  props: ["label", "image", "data"],
  data() {
    return {
        bgwhite: "bg-white",

    }
  },
  name: "menu-item",
  
};
</script>
