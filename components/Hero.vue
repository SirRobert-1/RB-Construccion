<template>
  <section
    class="hero pt-28 xl:pt-0 bg-blue w-full xl:mx-5 text-white flex flex-col justify-center items-center"
  >
    <h1 class="hero__title mb-16 text-center">
      Trabajos con más de 15 años de experiencia
    </h1>
    <div class="flex items-center mb-8">
      <img src="../assets/infoPersonal.svg" alt="" />
      <p class="ml-2 text-center">Técnico Especializado Raúl Basilio</p>
    </div>
    <div class="flex items-center mb-8">
      <img src="../assets/numWhats.svg" alt="" />
      <a href="https://wa.me/2282299992" target="_blank" class="ml-2"
        >22 82 29 99 92</a
      >
    </div>
    <div class="flex items-center mb-8">
      <img src="../assets/correo.svg" alt="" />
      <p class="ml-2">rawl.guzman7@gmail.com</p>
    </div>
    <div class="flex items-center mb-14">
      <img src="../assets/ubicacion.svg" alt="" />
      <p class="ml-2">C.P. 91210</p>
    </div>
    <img
      class="mx-auto mb-14 cursor-pointer"
      src="../assets/codeQr.svg"
      @click="ir('qr')"
      alt=""
    />
  </section>
</template>

<script>
export default {
  methods: {
    ir(url) {
      this.$router.push(url)
    },
  },
}
</script>
