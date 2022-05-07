<template>
  <div class="construccion bg-white mb-5">
    <img src="../assets/construccion.svg" alt="" />
    <h1 class="construccion__title flex justify-center">Construcción</h1>
    <p @click="verMas('lista')">Ver más</p>
    <img src="../assets/flecha.svg" alt="" />
    <ul v-if="this.vistaActiva == 'lista'">
      <li>Anivelamiento de terreno</li>
      <li>Remodelación y ampliaciones</li>
      <li>Construcción residencial</li>
      <li>Colocación de pisos y azulejos</li>
      <img src="../assets/flechaUp.svg" alt="" />
      <p @click="verMenos('cardCons')">Ver menos</p>
    </ul>
  </div>
</template>
<script>
export default {
  data() {
    return {
      vistaActiva: 'cardCons',
    }
  },
  methods: {
    verMas(lista) {
      this.vistaActiva = lista
    },
    verMenos(cardCons) {
      this.vistaActiva = 'cardCons'
    },
  },
}
</script>
