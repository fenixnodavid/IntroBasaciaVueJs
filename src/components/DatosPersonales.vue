<script setup>
const title = "Yamil D. Rueda";
const descripcion = "Tecnico Universitario en Programación - UTN";

const presentacion = "Hola, Bienvenido a mi porfolio de proyectos. Soy desarrollador web con experiencia en el desarrollo de aplicaciones web y moviles.";
const redesSociales = [
    {id:1, name: 'linkedin',src: '/src/assets/linkedin_icon.svg', URL: 'https://www.linkedin.com/in/yamil-rueda-7b490025a/'},
    {id:2, name: 'Instagram',src: '/src/assets/instagram_icon.svg', URL: 'https://www.instagram.com/institutozen?igsh=aDV3YXd1d3BtZWF5'},
    {id:3, name: 'github',src: '/src/assets/github_icon.svg', URL: 'https://github.com/fenixnodavid'},
    {id:4, name: 'curriculum',src: '/src/assets/cv_resume_icon.svg', URL: 'https://drive.google.com/file/d/1e3vGl8Z6wlS4tMVaZ5Rc4mCXW7johYlH/view?usp=sharing'},
];

</script>

<template>
<section class="datos-personales">
    <div class="card">
        <h1>{{title}}</h1>
        <h2>{{descripcion}}</h2>
        <p>{{presentacion}}</p>
        <ul class="container-lista">
            <li v-for="red in redesSociales" :key="red.id">
                <a :href="red.url"><img class="icon-redsoacial" :src="red.src" width="35rem" :alt="red.name"></a>
            </li>
        </ul>
        <h3>Mi telefono personal: +54 9 2604-847482</h3>
        <h4>San Rafael, Mendoza, Argentina</h4>
    </div>
</section>

</template>

<style scoped>
h1 {
font-size: 2.5rem;
}

p {
    font-size: 1.2rem;
    font-weight: 600;
    margin-bottom: 1rem;
}

.card {
    background-color: rgb(28, 41, 52);
    border-radius: 10px;
    margin: 10px;
    text-align: center;
}
.conteiner-lista {
    display: flex;
    justify-content: center;
    list-style: none;
    padding: 0;
    margin: 0;
    text-align: center;
}

.icon-redsocial {
    align-items: center;
    background-color: aliceblue;
    border-radius: 50%;
    padding: 2px;
    margin: 5px;
    box-shadow:  0 0 5px rgba(95, 124, 205, 0.934);
}

.icon-redsocial:hover{
    background-color: rgb(28, 41, 52);
    box-shadow: 0 0 5px rgba(251, 249, 249, 0.934);
}

h3{
    font-size: 1.2rem;
    font-weight: 600;
}
</style>