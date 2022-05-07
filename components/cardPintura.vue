<template>
  <div class="pintura bg-white mb-5">
    <img src="../assets/pintura.svg" alt="" />
    <h1 class="pintura__title flex justify-center">Pintura</h1>
    <p @click="verMas('lista')">Ver más</p>
    <img src="../assets/flecha.svg" alt="" />
    <ul v-if="this.vistaActiva == 'lista'">
      <li>Reparacion de superficies</li>
      <li>Lijado</li>
      <li>Preparación de colores</li>
      <li>Impermeabilización</li>
      <li>Revestimiento de paredes y techos</li>
      <li>Fibrado y asfáltico</li>
      <li>Reparación de grietas y agujeros</li>
      <img src="../assets/flechaUp.svg" alt="" />
      <p @click="verMenos('cardPint')">Ver menos</p>
    </ul>
  </div>
</template>
<script>
export default {
  data() {
    return {
      vistaActiva: 'cardPint',
    }
  },
  methods: {
    verMas(lista) {
      this.vistaActiva = lista
    },
    verMenos(cardPint) {
      this.vistaActiva = 'cardPint'
    },
  },
}
</script>
