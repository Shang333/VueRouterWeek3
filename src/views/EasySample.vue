<script setup>
// 區域註冊元件
import EasyHeader from '@/components/EasyHeader.vue';
import EasyCard from '@/components/EasyCard.vue';
import EasyFooter from '@/components/EasyFooter.vue';
import { ref } from 'vue';

const data = ref({
    title: '這是一張卡片',
    content:"ejfehfjknsdjfknwirewfnwlfklsd",
    imgUrl:'https://thumb.photo-ac.com/e7/e71cbebbdd8c2130a037b78c2d3f99d4_t.jpeg'
})

const editTitle = (newTitle) =>{
    console.log('editTitle:', newTitle);
    data.value.title = newTitle;
}

//props: 前內後外 通常會使用同名。單向數據流。內層資料不能改外層。
</script>

<template>
    <div class="container">
        <EasyHeader/> 
        <div class="col-4">
        <!-- <div class="row"> -->
            <!-- <div class="col-4" v-for="i in 10" :key="i"> -->
             <EasyCard v-bind:content="data" @emit-title="editTitle"/>  
            <!-- </div> -->
        </div>
        <EasyFooter/>
    </div>
</template>