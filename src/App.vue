<template>
  <div id="app">


          <div class="container mt-2">
        <div class="row">
          <div class="col text-center text-uppercase">
            <small>Lo ultimo en noticias</small>
            <h2>en desarrollo digital</h2>
          </div>
        </div>
      </div>

    <div class="container">
        <section-api></section-api>
      </div>


    <div class="container mt-5">
      <div class="row">
        <div class="col text-center text-uppercase">
          <small> nuestro </small>
          <h2>equipo</h2>
        </div>
      </div>  
    </div>
    <div class="container">
      <div class="row justify-content-center  mb-5">
        <div class="col mt-5 d-flex" v-for="(item, index) of equipo" :key="index">
          <team-card :member="item"></team-card>
        </div>
      </div>
    </div>

    <footer-page></footer-page>
  </div>
</template>

<script>
import TeamCard from "./components/TeamCard.vue";
import image from "../public/img/nicolleP.jpg";
import image1 from "../public/img/everC.jpg";
import image2 from "../public/img/moisesH.jpg";
import image3 from "../public/img/danielC.jpg";
import image4 from "../public/img/danielL.jpg";
import FooterPage from './components/FooterPage.vue';
import SectionApi from './components/SectionApi.vue';

export default {
  components: { TeamCard, FooterPage, SectionApi },
  name: 'App',
    data() {
    return {
      equipo: [
        {
          codigo: 1,
          nombre: "Nicolle Palomo",
          descripcion:
            "Estudio en el SENA, tengo 29 años, me gusta muchísimo la música y fotografía.",
          rol: "Desarrollador frontend",
          imagen: image,
        },
        {
          codigo: 2,
          nombre: "Ever Cano",
          descripcion:
            "Estudio en la Corporación universitaria Minuto de Dios, tengo 26 años, me gusta ver series, peliculas, salir a viajar, en mis tiempos libres suelo jugar videojuegos.",
          rol: "Desarrollador backend",
          imagen: image1,
        },
        {
          codigo: 3,
          nombre: "Moises de la Hoz",
          descripcion:
            "Estudio en la Universidad del Norte, tengo 21 años, mis pasatiempos son leer, jugar videojuegos y jugar tenis, soy fan del Legendarium de Tolkien.",
          rol: "Analista de desarrollo",
          imagen: image2,
        },
        {
          codigo: 4,
          nombre: "Daniel Cuellar",
          descripcion:
            "Estudio en el SENA, tengo 25 años, mis pasatiempos son las series, los videojuegos y el anime, me gustan los retos y el autoaprendizaje continuo.",
          rol: "Tester",
          imagen: image3,
        },
        {
          codigo: 5,
          nombre: "Juan Daniel",
          descripcion:
            "Estudia en la Corporación universitaria Minuto de Dios, tengo 20 años, mi pasatiempo es ver películas, jugar videojuegos, soy un muchacho noble, tímido pero juicioso.",
          rol: "Bases de Datos",
          imagen: image4,
        },
      ],
    };
  },
}
</script>

