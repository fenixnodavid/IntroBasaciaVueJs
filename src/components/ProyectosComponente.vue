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
    id: 2,
    src: "src/assets/IZ logo 2.png",
    titulo: "Plataforma de terapias alternativas",
    descripcion: "Diseñe una plataforma en la cual contiene toda la inforacion dediferentes terapias alternativas",
    projectoLink: "https://www.facebook.com/intitutozen/",
    githubLink: "https://github.com/fenixnodavid/HolaMundo"
},
{
    id: 3,
    src: "src/assets/simple-karate-logo-vector.jpg",
    titulo: "Blog de karate",
    descripcion: "Constui un Blog sobre Karate con informacion el arte marcial y su deporte.",
    projectoLink: "https://www.instagram.com/dojozensanrafaelok/reel/DB_hloKucQU/",
    githubLink: "https://github.com/fenixnodavid/desktop-tutorial"
},
{
    id: 4,
    src: "src/assets/EL EMPERADOR (Ver. Mitologico).jpg",
    titulo: "Aplicacion l Emperador",
    descripcion: "Esta aplicacion te enseña todo lo que nu Emperador debe hacer",
    projectoLink: "https://wordpress.com/home/institutozen.wordpress.com",
    githubLink: "https://github.com/fenixnodavid/Primer-repositoro"
}
]);

</script>

<template>
    <!-- Aquiva ek codigo HTML de la galeria de proyecto-->
    <div class="galeria">
        <!-- Itera sobre cada proyecto en la lista de misProyectos -->
         <!-- key es una propiedad especial que se utiliza para identificar de forma unica cada elemento en una lista de Vue.js -->
        <li class="proyecto" v-for="proyecto in misProyectos" :key="proyecto.id">
            <!-- muestra la imagen del proyecto utilizando : que es una directiva de enlace en Vue.js -->
             <img :src="proyecto.src" :alt="proyecto.itulo">
             <div class= "proyecto-info">
                <!-- Muestra el titulo y la descripcion del proyecto utilizando la interpolacion de Vue.js-->
                 <h3>{{ proyecto.titulo }}</h3>
                 <p>{{ proyeto.descripcion }}</p>
                 <div class="proyecto-links">
                    <a :href="proyecto.projectoLink" class="btn-ver-mas" target="_blank" rel="noopener noreferrer">Ver
                        Proyecto</a>
                    <a :href="proyecto.githubLink" class="github-link" target="_blank" rel="noopener noreferrer">Ver
                        Código en GiHhub</a>
                 </div>    
             </div>
        </li>
    </div>
</template>

<style scoped>
/*Estilos Fondo Animado de Css de la galeria*/
/*La clase 'galeria' es el contenedor principal de la galeria de proyectos */
.galeria{
    width: 100%; /* Establece el ancho de la galeria al 100% del contenedor padre */ 
    height: 100; /* Establece la altura de la galeria al 100% del contenedor padre */
    display: flex; /* Utiliza flebox para organizar los elementos hijos en la galeria */
    flex-wrap: wrap;/* permite que los elemntos se ajuusten y pasen a la siguiente linea si no caben en una sola fila */
    gap: 20px;/* Establece un espacio de 20px entre los elementos de la galeria */ 
    padding: 20px;/* agrega un padding de 20px alrededor de la galeria */
    justify-content: center;/* Centra los elmentos hijos horizontalmente */
    background: linear-gradient(-45deg,#021526, #0334E6, #6EACDA, #E2E286); /* Aplica un fondo con un degradado de colores */

    background-image: url('/src/assets/fondo-proyectos.jpg'); 
   /*Ajusta el tamaño del fondo para que cubra el area complea */
    background-size: 400% 400%;
    /*Aplica un animacion al fondo que dura 15 segundos, tiene una transicion suave y se repite indefinidamente */
    animation: gradiaent 15s ease infinite;

    background-position: center;
    background-repeat: no-repeat; 
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

}
/* La clase 'proyecto' es el contenedor individual de cada proyecto */
.proyecto {
    /* Utiliza flebox para organizar el contenido de lproyecto en una columna */
    display: flex;
    /* Establece la direcion de los elementos en columna */
    flex-direction: column;
    /* Aplica  un borde de 2px solido y color gris claro (#ddd) alrededor del proyecto */
    border: 2px solid #ddd;
    /* Redondea las esquinas del contenedor */
    border-radius: 8px;
    /* Oculta cualquier contenido que se desborde del contenedor */
    overflow: hidden;
    /* Establece un color de fondo claro para el proyecto */
    background-color: #f9f9f9;
    /* Define el ancho maximo del proyecto en 222px */
    max-width: 222px;
    /* Hace que el contenedor se ajuste flexiblemente ocupado al menos 300px de ancho */
    flex: 1 1 300px;
}

/* Estilo para las imagenes dentro del contenedor 'Proyecto' */
.proyecto img {
    /* Hace que la imagen ocupe el 100% del ancho del contenedor */
    width: 100%;
    /* Mantiene la relacion de aspecto de la imagen */
    height: auto;
    /* Asegura que la imagen se muestre como un bloque, sin espacio en linea alrededor */
    display: block;
}

/* Clase 'proyecto-info' contiene la informacion del proyecto */
.proyecto-info {
    /* Agrega un padding de 15px alrededor de la informacion */
    padding: 15px;
    /* centra el texto dentro del contenedor */
    text-align: center;
}

/* Estilo para los titulos de los proyectos */
.proyecto-info h3 {
    /*Establece un margen superior e inferior de 10px */
    margin: 10px 0;
    /* Define el tamaño de la fuente a 1.3em (relativo al tamaño de fuente del contenedor) */
    font-size: 1.3em;
    /* Aplica un color gris oscuro (#333) al texto */
    color: #333;
}
/* Estilo para los parrafos de los proyectos */
.proyecto-info p {
    /* Establece un margen superior e inferior de 10px */
    margin: 10px 0;
    /* Define el tamaño de la fuente a 1em (igual al tamaño de fuente base) */
    font-size: 1em;
    /* Aplica un color gris (#666) al texto */
    color: #666;
}

/* La clase 'proyecto-links' organiza los enlaces y botone del proyecto */
.proyecto-links {
    /* Utiliza flexbox para organizar los enlaces en una columna */
    display: flex;
    /* Establece la direccion en los elementos en columna */
    flex-direction: column;
    /* Establece un espacio de 10px entre los elmentos */
    gap: 10px;
    /* Agrega un margen superior de 10px */
    margin-top: 10px;
}


</style>