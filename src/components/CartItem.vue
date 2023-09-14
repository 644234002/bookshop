<template>
    <div class="cart-item" >
    
        <b>{{cartItem.title}}</b><br />
        <b>Price:</b> {{cartItem.price}}<br />
        <b>Qty:</b> {{cartItem.qty}} ฿<br />
        <div align="center" style="margin-top: 1rem;">
            <button class="btn btn-success" ><i class="bi bi-plus"></i></button>&nbsp;
            <button class="btn btn-info" ><i class="bi bi-dash"></i></button>&nbsp;
            <button class="btn btn-danger" ><i class="bi bi-trash-fill"></i></button>
        </div>
    
    </div>
</template>

<script setup>
import { ref } from 'vue'

// props, emit
const props = defineProps(['cartItem'])
const cartItem =ref(props.cartItem)


// Increase



// Decrease




// Remove

</script>

<style  scoped>

</style>