<script setup>
import { ref } from 'vue'

const users = ["Pepe","Ana", "Juana","Lola","Suana","Marrana"]

const isChecked = ref(true)
</script>
<template>
    <ul>
        <li v-for="(user, index) in users" :key="index">{{ index }} {{ user }}</li>
    </ul>


    <!-- Single checkbox, boolean value: -->
    <input type="checkbox" id="check" v-model="isChecked" />
    <label for="checkbox">Pinchame {{ checked }}</label>

    <div class="bg-blue-400 font-mono text-white rounded py-1 px-2 w-24 flex justify-center items-center cursor-default"
    :class="{'bg-orange-500 font-bold': isChecked}">
        Este es el mensaje
    </div>


    <div v-show="false" class="">
        Este es un mensaje que se podria ocultar
    </div>

    <div v-if="false" class="">
        Este es un mensaje que se podria ocultar
    </div>

    <div v-else>
        esto se ve porque no cumplió la condición del if
    </div>
</template>