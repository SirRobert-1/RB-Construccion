<template>
  <section class="cardDesktop bg-white rounded-3xl h-40 px-5 my-40">
    <div class="flex my-5">
      <button
        @click="seleccionarServicio(servicio.id, servicio.info)"
        :class="
          servicioActivo == servicio.id ? 'bg-white  text-blue ' : 'bg-blue '
        "
        class="
          mx-1
          text-white
          px-5
          py-2
          border border-blue
          rounded-full
          flex
          justify-center
          items-center
          w-48
        "
        v-for="(servicio, index) of servicios"
        :key="index"
      >
        <img
          class="mx-2"
          :src="servicioActivo == servicio.id ? servicio.icon : servicio.iconW"
          alt=""
        />
        {{ servicio.titulo }}
      </button>
    </div>
    <div>
      <ul class="my-5">
        <li v-for="(info, index) of infoActiva[0]" :key="index">
          {{ info }}
        </li>
      </ul>
    </div>
  </section>
</template>
<script>
import electricaW from '@/assets/electricidadW.svg'
import hidroW from '@/assets/fontaneriaW.svg'
import construccionW from '@/assets/construccionW.svg'
import pinturaW from '@/assets/pinturaW.svg'
import airesW from '@/assets/airesW.svg'
import electrica from '@/assets/electricidad.svg'
import hidro from '@/assets/fontaneria.svg'
import construccion from '@/assets/construccion.svg'
import pintura from '@/assets/pintura.svg'
import aires from '@/assets/aires.svg'
export default {
  created() {
    this.infoActiva.push(this.default)
  },
  data() {
    return {
      servicioActivo: 'electrico',
      infoActiva: [],
      default: [
        'Baja tensión',
        'Instalación residencial',
        'Instalación tipo industrial',
        'Tablero de distibución',
        'Conocimiento en manejo de circuitos',
      ],
      servicios: [
        {
          id: 'electrico',
          icon: electrica,
          iconW: electricaW,
          titulo: 'Instalación eléctrica',
          info: [
            'Baja tensión',
            'Instalación residencial',
            'Instalación tipo industrial',
            'Tablero de distibución',
            'Conocimiento en manejo de circuitos',
          ],
        },
        {
          id: 'hidro',
          icon: hidro,
          iconW: hidroW,
          titulo: 'Instalación hidrosanitaria',
          info: [
            'Suministro de agua para consumo',
            'Evacuación de aguas residuales',
            'Calentador solar',
            'Mantenimiento a boiler',
            'Bomba-cisterna-tinaco',
            'Aguas pluviales',
          ],
        },
        {
          id: 'construccion',
          icon: construccion,
          iconW: construccionW,
          titulo: 'Construcción',
          info: [
            'Anivelamiento de terreno',
            'Remodelación y ampliaciones',
            'Construcción residencial',
            'Colocación de pisos y azulejos',
          ],
        },
        {
          id: 'pintura',
          icon: pintura,
          iconW: pinturaW,
          titulo: 'Pintura',
          info: [
            'Reparacion de superficies',
            'Lijado',
            'Preparación de colores',
            'Impermeabilización',
            'Revestimiento de paredes y techos',
            'Fibrado y asfáltico',
            'Reparación de grietas y agujeros',
          ],
        },
        {
          id: 'aires',
          icon: aires,
          iconW: airesW,
          titulo: 'Aires acondicionados',
          info: [
            'Instalación de equipos nuevos',
            'Revisión de buen funcionamiento de A.C.',
          ],
        },
      ],
    }
  },
  methods: {
    seleccionarServicio(id, info) {
      this.servicioActivo = id
      this.infoActiva = []
      this.infoActiva.push(info)
    },
  },
}
</script>

<style lang="scss" scoped>
.cardDesktop {
  height: 494px;
}
</style>