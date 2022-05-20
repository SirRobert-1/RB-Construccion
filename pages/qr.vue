<template>
  <div
    class="
      qr
      bg-blue
      flex flex-col
      justify-center
      items-center
      w-screen
      h-screen
    "
  >
    <img class="w-80 h-80" src="../assets/qr-code.svg" alt="" />

    <button
      @click="ir('/')"
      class="hero__p flex justify-center text-white mt-10"
    >
      Volver al Inicio
    </button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      vistaActiva: 'contacto',
    }
  },
  methods: {
    cambiarVista(vista) {
      this.vistaActiva = vista
    },
    ir(url) {
      this.$router.push(url)
    },
  },
}
</script>

