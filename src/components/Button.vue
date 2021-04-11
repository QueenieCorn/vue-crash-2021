<template>
    <button @click="onClick()" :style="{ background:color }" class="btn"> {{text}} </button> 
    <!-- v-on:click="onClick() or @click="onClick()" " -->

</template>

<script>
export default {
    name: 'Button',
    props : {
        text:String,
        color: String
    },
    methods: {
        onClick() {
            console.log('click')
        }
    }
}
</script>

<style>
    
</style>