<script setup>
import { ref } from 'vue';
const arreglo= ref([
{id:1, fecha:'2024', titulo:'Tecnico Universitario en Programación', descripcion:'Lenguaje de Java, Python, JavaScript, VisualStudioCode, PyCharm, NetBeans Git Hub y Git Bash', enlace:"http"},
{id:2, fecha:'2023', titulo:'Informatica basica', descripcion:'Conocimiento a nivel de usuario de Microsoft Office (Word, Excel, Access y Power Point), Conocimiento avanzado de Adobe Photoshop cs. Cursado en la universidad Santísima Trinidad. Conocimiento avanzado en Autocad.',enlace:"http"},
{id:3, fecha:'2022', titulo:'Curso de composición fotográfica r', descripcion:'De interiores y exteriores en la universidad Santísima Trinidad', enlace:"http"},
]);
</script>

<template>
<h1>Linea de Tiempo</h1> 
<ul>
<li v-for="item in arreglo" :Key="item.id">
<div class="fecha">{{item.fecha}}</div>
<div class="titulo">{{item.titulo}}</div>
<div class="descripcion">{{item.descripcion}}</div>
<a class="enlace">{{item.enlace}}</a>
</li>
<!-- <li>
<div class="fecha">2024</div>
<div class="titulo">titulo</div>
<div class="descripcion">De esta forma es como se puede crear una linea de tiempo basica una vez echo este modelo podemos ya
representarlo en vue o si no...</div>
<a class="enlace">enlace al titulo</a>
</li>
<li>
<div class="fecha">fecha</div>
<div class="titulo">titulo</div>
<div class="descripcion">descripcion</div>
<a class="enlace">enlace al titulo</a>
</li>
<li>
<div class="fecha">fecha</div>
<div class="titulo">titulo</div>
<div class="descripcion">descripcion</div>
<a class="enlace">enlace al titulo</a>
</li> -->
</ul>
</template>

<style>
ul{
border-left: 3px solid;
margin-left: 2rem;
}
li{
list-style: decimal;
padding-left: 1rem;
}
.fecha{
background-color:antiquewhite;
color: black;
border-bottom: 3px solid;
}
.titulo{
display:flex;
justify-content: center;
}
.descripcion{
padding: 1rem;
}
.enlace{
display: flex;
justify-content: center;
}
</style>