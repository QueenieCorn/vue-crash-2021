<template lang="">

    <header>
            <h1>{{ title }}</h1>
            <Button text="Add Task" color="green"/>
            <!-- <Button text="Update Task" color="blue"/>
            <Button text="Delete Task" color="red"/> -->
    </header>

</template>
<script>

import Button from './Button'

export default {
    name: 'Header',
    // props: ['title'],
    props: {
        title: String,
        // title: {
        //     type: String,
        //     default: 'Hello World',
        // }
    },
    components: {
        Button,
    }
}
</script>

<style scoped>
    header{
        display: flex;
        justify-content:space-between;
        align-content: center;
        margin-bottom: 20px;
    }
</style>