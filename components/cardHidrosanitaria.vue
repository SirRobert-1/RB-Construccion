<template>
  <div class="fontaneria bg-white mb-5">
    <img src="../assets/fontaneria.svg" alt="" />
    <h1 class="fontaneria__title flex justify-center">
      Instalación Hidrosanitaria
    </h1>
    <p @click="verMas('lista')">Ver más</p>
    <img src="../assets/flecha.svg" alt="" />
    <ul v-if="this.vistaActiva == 'lista'">
      <li>Suministro de agua para consumo</li>
      <li>Evacuación de aguas residuales</li>
      <li>Calentador solar</li>
      <li>Mantenimiento a boiler</li>
      <li>Bomba-cisterna-tinaco</li>
      <li>Aguas pluviales</li>
      <img src="../assets/flechaUp.svg" alt="" />
      <p @click="verMenos('cardHidro')">Ver menos</p>
    </ul>
  </div>
</template>
<script>
export default {
  data() {
    return {
      vistaActiva: 'cardHidro',
    }
  },
  methods: {
    verMas(lista) {
      this.vistaActiva = lista
    },
    verMenos(cardHidro) {
      this.vistaActiva = 'cardHidro'
    },
  },
}
</script>
