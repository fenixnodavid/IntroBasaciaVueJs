<script setup>
// Este componente muestra una galeria de proyectos coninformacion sobre cada proyecto
import { ref } from 'vue';
// .ref es una funcion que se utiliza para crear una referencia reactiva en Vue 3
var misProyectos = ref([]);
// .value es una propiedad que se utiliza para acceder al valor de una referencia reactiva en Vue 3
misProyectos.value = ([
// esto es un array de objetos que contiene informacion sobre los proyectos
{
    id: 1,
    src:"src/assets/EL MAGO (Ver. Mitologico).jpeg",
    titulo: "Aplicacion para Lectura de Tarot",
    descripcion: "Cree una aplicacion para celular, donde érmite conocer los arcanos y las demas cartas aprender a tirar las cartas",
    projectoLink: "https://www.instagram.com/institutozen/?hl=es",
    githubLink: "https://github.com/fenixnodavid/IntroBasaciaVueJs"
},
{
    
}
])

</script>

<template>
    <div class="galeria">
        <div class="proyecto">
            <img src="src/assets/EL MAGO (Ver. Mitologico).jpeg" alt="Proyecto 1">
            </div class="proyecto-info">        
                <h3>Tarot</h3>
                <p>Cree una app sobre lectura de tarot</p>
                <div class="proyecto-links">
                    <a href="https://www.instagram.com/institutozen/?hl=es" class=" btn-ver-mas" target="_blank" rel="noopener noreferrer">ver 
                        Proyecto</a>
                    <a href="https://github.com/fenixnodavid/IntroBasaciaVueJs" class="github-link" target="_blank"
                        rel="noopener noreferrer">ver Codigo en GitHub</a>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
/*Estilos Fondo Animado de Css de la galeria*/
/*La clase 'galeria' es el contenedor principal de la galeria de proyectos */
.galeria{
/* Establece el ancho de la galeria al 100% del contenedor padre */ 
    width: 100%;
    /* Establece la altura de la galeria al 100% del contenedor padre */
    height: 100;
    /* Utiliza flebox para organizar los elementos hijos en la galeria */
    display: flex;
    /* permite que los elemntos se ajuusten y pasen a la siguiente linea si no caben en una sola fila */
    flex-wrap: wrap;
    /* Establece un espacio de 20px entre los elementos de la galeria */
    gap: 20px;
     /* agrega un padding de 20px alrededor de la galeria */
    padding: 20px;
    /* Centra los elmentos hijos horizontalmente */
    justify-content: center;
    /* Aplica un fondo con un degradado de colores */
    background: linear-gradient(-45deg,#021526, #0334E6, #6EACDA, #E2E286);

    /* background-image: url('/src/assets/fondo-proyectos.jpg'); */
    /* Ajusta el tamaño del fondo para que cubra el area complea */
    background-size: 400% 400%;
    /* Aplica un aanimacion al fondo que dura 15 segundos, tiene una transicion suave y se repite indefinidamente */
    animation: gradiaent 15s ease infinite;

    /* background-position: center;
    background-repeat: no-repeat; */
}
 /*Defin una animacion llada 'gradient' para cambiar la posicion del fondo */
 @keyframes gradient {
    /* Al inicio. el fondo estaposicionado en el 0% horizontal y 20% vertical */
    0% {
        background-position: 0% 50%;
    }
    50% {
        background-position: 100% 50%;
    }
    100% {
        background-position: 0% 50%;
    }

};


</style>