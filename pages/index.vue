<template>
  <div class="index bg-blue relative flex flex-col items-center">
    <img
      class="hero_logo left-0 right-0 mx-auto -mt-20 absolute"
      src="../assets/LogoCirculo.svg"
      alt=""
    />
    <Hero v-if="this.vistaActiva == 'contacto'" />
    <button
      v-if="this.vistaActiva == 'contacto'"
      @click="cambiarVista('trabajo')"
      class="hero__p flex justify-center text-white"
    >
      Ver trabajos
    </button>
    <Trabajos v-if="this.vistaActiva == 'trabajo'" />
    <button
      v-if="this.vistaActiva == 'trabajo'"
      @click="cambiarVista('contacto')"
      class="hero__p flex justify-center text-white -mt-2"
    >
      Ver contacto
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
  },
}
</script>
<style lang="scss" scoped>
.index {
  height: calc(100vh - 10rem);
  margin-top: 10rem;
}
</style>
