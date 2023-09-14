<template>
    <div>
        
        <div v-for="book in books">
            <!-- BookItem -->
            <!-- ส่งค่า book ไป props book ใน BookItem.vue -->
            <BookItem v-bind:book="book" v-on:addBookItem="AddToCart"/>
            
        </div>
    </div>
</template>

<script setup>
import { ref } from 'vue'
//import BookItem
import BookItem from './BookItem.vue'


// props, emit
//สร้าง props เป็น books
const props = defineProps(['books'])
const books = ref(props.books) //เอา props เก็บเข้าตัวแปรอีกที
const emit = defineEmits(['addBook'])

// AddToCart
function AddToCart(book){
    emit( 'addBook' , book )
}


</script>

<style  scoped>

</style>