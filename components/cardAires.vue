<template>
  <div class="aires bg-white mb-5">
    <img src="../assets/aires.svg" alt="" />
    <h1 class="aires__title flex justify-center">Aires acondicionados</h1>
    <p @click="verMas('lista')">Ver más</p>
    <img src="../assets/flecha.svg" alt="" />
    <ul v-if="this.vistaActiva == 'lista'">
      <li>Instalación de equipos nuevos</li>
      <li>Revisión de buen funcionamiento de A.C.</li>
      <img src="../assets/flechaUp.svg" alt="" />
      <p @click="verMenos('cardAires')">Ver menos</p>
    </ul>
  </div>
</template>
<script>
export default {
  data() {
    return {
      vistaActiva: 'cardAires',
    }
  },
  methods: {
    verMas(lista) {
      this.vistaActiva = lista
    },
    verMenos(cardaires) {
      this.vistaActiva = 'cardAires'
    },
  },
}
</script>
