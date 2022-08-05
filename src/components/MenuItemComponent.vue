<template>
    <div class="bg-neutral-700 h-screen w-full border-slate-200 border-y-2 rounded-md">
        <div class="items-center text-white mx-auto py-10 px-8">
            <h2 class="pt-5 text-4xl font-bold text-center">{{label}}</h2>
            <img class="self-center rounded-md h-auto w-full my-5 mx-0 shadow-lg shadow-black max-w-full" :src="require(`../assets/img/${image}.jpg`)"  alt="Fotoğraf">
            <div class="justify-between text-md">
                <ul>
                    <li v-for="(item,index) in data" :key="index"><span style="float: left;"> {{item.label}}</span> : <span style="float:right;">{{item.price}} TL</span></li>
                    
                </ul>
            </div>
        </div>

        <!-- <div class="label">
            <p v-if="icon" class="metarialicon">{{icon}}</p>
            <span>{{label}}</span>
        </div>
        <div class="items">
            <menu-item 
            v-for="(item,index) in data"
            :key="index"
            :label="item.label"
            :price="item.price"
            :desc="item.desc"
            ></menu-item>
        </div> -->
        
        <style>
                    .single-menu-item {
                    width: 100%;
                    display: flex;
                    flex-direction: column;
                    margin: 20px 0;
                }

                .single-menu-item .menu-item-header {
                    display: flex;
                    justify-content: space-between;
                    font-size: 1.1rem;
                }

                .menu-item-description {
                    margin-top: 5px;
                    padding: 10px 0;
                    font-size: 0.9rem;
                }
                </style>
                <div class="sub_category" v-for="(category,index) in data.menu">
                    <div class="sub_category_name">{{category.label}}</div>
                    <div class="single-menu-item" v-for="(item,index) in category.children">
                        <div class="menu-item-header">
                            <p class="menu-item-name">{{item.label}}</p>
                            <p class="menu-item-desc">{{item.desc}}</p>
                            <p>{{item.price}}</p>
                        </div>
                    </div>
                </div>
        
        
        
    </div>
</template>

<script>
export default {
    props: ["label","image","data"],
    name: "menu-item",

}
</script>
