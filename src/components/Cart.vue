<template>
    <div>
        <div v-if="props.cart.length>0" v-for="item in props.cart">
            <!-- CartItem --> 
            <CartItem :cartItem="item"/>

            
        </div>
        <div >
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
//const cart =ref(props.cart)


// Increase



// Decrease




// Remove



</script>

<style  scoped>

</style>