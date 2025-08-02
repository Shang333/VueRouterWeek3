<script setup>
import { ref } from 'vue';

const imgUrl = ref('https://thumb.photo-ac.com/e7/e71cbebbdd8c2130a037b78c2d3f99d4_t.jpeg')
const num = ref(1);
const add = ()=>{
    num.value++ //卡片的數字狀態各自獨立
}
</script>

<template>
    <div class="card">
        <img :src="imgUrl" alt="..."/>
        <div class="card-body">
            <h5 class="card-title">card title {{ num }}</h5>
            <p class="card-text">AGHHDJWDBWJDKQWJEQNDQJNQKJDNJWNJDNWJNDJQNBDBHghfdjwq12</p>
            <a href="#" class="btn btn-primary" @click.prevent="add">Go somewhere</a>
        </div>
    </div>
</template>