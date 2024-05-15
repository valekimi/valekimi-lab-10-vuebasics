<script setup>
import {ref} from 'vue'
const items = ref (['Home', 'Projects', 'Services', 'Contacts'])
</script>

<template>
 <nav>
    <h1>Is a Navbar!</h1>
    <ul>
        <li v-for="item in items">{{ item }}</li>
    </ul>
 </nav>
</template>

<style scoped>
ul {
    width: 100%;
   padding: 0 200px;
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
    gap: 40px;
}

li {
    list-style: none;
}
</style>