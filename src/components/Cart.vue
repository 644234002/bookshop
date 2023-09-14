<template>
    <div>
        <div v-if="props.cart.length>0" v-for="item in props.cart">
            <!-- CartItem --> 
            <CartItem :cartItem="item" @increaseCartItem="Increase" @decreaseCartItem="Decrease" @removeCartItem="Remove"/>

            
        </div>
        <div v-else>
            <div class="cart-empty" >
                <img src="../assets/empty.png" style="height: 130px;" alt="" srcset="">
            </div>
        </div>
    </div>
</template>

<script setup>
import { ref } from 'vue'
//import CartItem
import CartItem from '../components/CartItem.vue'

// props, emit
const props = defineProps(['cart'])
const emit = defineEmits(['increaseCart'])
//const cart =ref(props.cart)


// Increase
function Increase(bookid){
    emit('increaseCart',bookid)
}


// Decrease
function Decrease(bookid){
    emit('decreaseCart',bookid)
}

//Homwork
function Remove(bookid){
    emit('removeCart',bookid)
}



// Remove
//Homework


</script>

<style  scoped>

</style>