<!-- eslint-disable vue/multi-word-component-names -->
<script setup>
import { ref } from 'vue';
const titulo= 'Desarrollador Full Stack';
const fecha= 'Desde Enero 2022/ / Julio 2024';
const experiencias = ref([
    {id:1, src:'src/assets/availability-svgrepo-com.svg', parrafo: 'Lidere un equipo'},
    {id:2, src:'src/assets/dns-svgrepo-com.svg', parrafo: 'Diseño y Desarrollo e Reels'},
    {id:3, src:'src/assets/flexible-access-svgrepo-com.svg', parrafo: 'Soluciones de grupos'},
    {id:4, src:'src/assets/machine-vision-svgrepo-com.svg', parrafo: 'Colabore en Capacitaciones'},
    {id:5, src:'src/assets/system-settings-svgrepo-com.svg', parrafo: 'Automatice mineria'},

]);
</script>

<template>
    <div class="card">
        <h3 class="titulo">{{titulo.toLocaleUpperCase()}}</h3>
        <p class="fecha">{{fecha}}</p>
        <ul class="listado">
            <li class="item" v-for="experiencia in experiencias" :key="experiencia.id">
                <img class="imagen-svg" :src="experiencia.src" width="45rem" :alt="experiencia.parrafo">
                <p>{{ experiencia.parrafo }}</p>
            </li>
        </ul>
    </div>

    
</template>
<style scoped>
.card{
    display: flex;
    flex-direction: column;
    padding: 2rem;
    background-color: rgb(28, 41, 52);
    border-radius: 15px;
}
.titulo{
    font-size: 1.5rem;
    color: coral;
    
}
.fecha{
    font-size: 1rem;
    color: burlywood;
    margin-bottom: 1rem;
}
.listado{
    display: flex;
    flex-direction: column;
}
.item{
    align-items: center;
    display: flex;
    padding: 1rem;
    gap: 1.5rem;
}
</style>