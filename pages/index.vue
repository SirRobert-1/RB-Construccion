<template>
  <div class="index bg-blue relative flex flex-col items-center xl:px-10 pb-10">
    <img
      class="hero_logo left-0 right-0 mx-auto -mt-20 absolute"
      src="../assets/LogoCirculo.svg"
      alt=""
    />
    <div class="flex flex-col xl:flex-row xl:items-start items-center">
      <Hero v-if="this.vistaActiva == 'contacto'" class="xl:mt-44" />
      <button
        v-if="this.vistaActiva == 'contacto'"
        @click="cambiarVista('trabajo')"
        class="hero__p flex justify-center text-white xl:hidden"
      >
        Ver trabajos
      </button>
      <Trabajos v-if="this.vistaActiva == 'trabajo'" />
      <TrabajosDesktop class="hidden xl:block" />
      <button
        v-if="this.vistaActiva == 'trabajo'"
        @click="cambiarVista('contacto')"
        class="hero__p flex justify-center text-white mt-2"
      >
        Ver contacto
      </button>
    </div>
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
  height: 100%;
  margin-top: 10rem;
  @include screen(tablet) {
    //height: calc(100vh - 10rem);
    height: 100%;
  }
}
</style>
