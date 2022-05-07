<template>
  <div
    :class="vistaActiva ? 'rounded-3xl' : 'rounded-full'"
    class="flex flex-col justify-center items-center bg-white text-blue mb-5 w-full py-2"
  >
    <div class="flex items-center">
      <img class="mr-2" :src="icon" alt="" />
      <h1 class="flex justify-center">
        {{ titulo }}
      </h1>
    </div>
    <ul v-if="vistaActiva" class="my-5">
      <li v-for="(servicio, index) of info" :key="index">{{ servicio }}</li>
    </ul>
    <div
      class="flex flex-col justify-center items-center"
      v-if="!vistaActiva"
      @click="verMas()"
    >
      <p>Ver más</p>
      <img src="../assets/flecha.svg" alt="" />
    </div>
    <div
      class="flex flex-col justify-center items-center"
      v-if="vistaActiva"
      @click="verMas()"
    >
      <img src="../assets/flechaUp.svg" alt="" />
      <p>Ver menos</p>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      vistaActiva: false,
    }
  },
  methods: {
    verMas() {
      this.vistaActiva = !this.vistaActiva
    },
  },
  props: {
    icon: {
      type: String,
      required: true,
    },
    titulo: {
      type: String,
      required: true,
    },
    info: {
      type: Array,
      required: true,
    },
  },
}
</script>
