<template>
    <div class="container">
        <div class="buttons-group">
            <button
                type="button"
                :class="{
                    active: currentTab === 'home'
                }"
                @click="tabChangeHandler('home')"
            >Home</button>
            <button
                type="button"
                :class="{
                    active: currentTab === 'products'
                }"
                @click="tabChangeHandler('products')"
            >Projects</button>
            <button
                type="button"
                :class="{
                    active: currentTab === 'services'
                }"
                @click="tabChangeHandler('services')"
            >Services</button>
            <button
                type="button"
                :class="{
                    active: currentTab === 'contact'
                }"
                @click="tabChangeHandler('contact')"
            >Contact</button>
        </div>
        <div class="content">
            <p>You chose <span class="highlight">{{currentTab}}</span></p>
        </div>
    </div>
</template>

<script setup>
import { ref } from 'vue';
const currentTab = ref('home');

const tabChangeHandler = (tabName) => {
    currentTab.value = tabName;
}
</script>
<style>
.buttons-group {
    margin-bottom: 10px;
}
button {
    display: inline-block;
    padding: 18px 30px;
    color: #fff !important;
    font-weight: bold;
    font-size: 16px;
    text-decoration: none !important;
    line-height: 1;
    text-transform: uppercase;
    background-color: transparent;
    -webkit-transition: background-color 0.25s;
    -moz-transition: background-color 0.25s;
    transition: background-color 0.25s;
    background: #389dc1;
}
button.active {
    background-color: #e35885
}
.content {
    text-align: center;
}
.highlight {
    color: #ffffff;
    display: inline-block;
    padding: 5px 10px;
    background-color: #c4d7e0;
    border-radius: 2px;
    text-transform: uppercase;
    font-size: 18px;
}
</style>
