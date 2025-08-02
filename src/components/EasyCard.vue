<script setup>
import { ref } from 'vue';
import { defineProps } from 'vue';

const imgUrl = ref('https://thumb.photo-ac.com/e7/e71cbebbdd8c2130a037b78c2d3f99d4_t.jpeg')
// const num = ref(1);
// const add = ()=>{
//     num.value++ //卡片的數字狀態各自獨立
// }

defineProps(['content'])

const emit = defineEmits(['emitTitle'])
const editOuterTitle= ()=>{
    console.log("內層觸發emit");
    emit('emitTitle','內層要修改外層的值')
}
</script>

<template>
    <div class="card">
        <img :src="imgUrl" alt="..."/>
        <div class="card-body">
            <!-- <h5 class="card-title">card title {{ num }}</h5> -->
            <h5 class="card-title">{{ content.title }}</h5>
            <p class="card-text">{{ content.content }}</p>
            <!-- <a href="#" class="btn btn-primary" @click.prevent="add">Go somewhere</a> -->
            <a href="#" class="btn btn-primary" @click.prevent="editOuterTitle">Go somewhere</a>
        </div>
    </div>
</template>