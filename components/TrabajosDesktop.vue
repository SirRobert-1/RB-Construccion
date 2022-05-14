<template>
  <section class="cardDesktop bg-white rounded-3xl h-40 px-5 my-40">
    <div class="flex my-5">
      <button
        @click="
          seleccionarServicio(servicio.id, servicio.info, servicio.images)
        "
        :class="
          servicioActivo == servicio.id ? 'bg-white  text-blue ' : 'bg-blue '
        "
        class="mx-1 text-white px-5 py-2 border border-blue rounded-full flex justify-center items-center w-48"
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
    <div class="flex flex-wrap justify-around">
      <img
        class="mx-2 w-20 h-20 object-cover"
        :src="image"
        alt=""
        v-for="(image, index) of imagesActivas[0]"
        :key="index"
      />
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
import bajaTension from '@/assets/Rb/bajaTension.jpg'
import bajaTension2 from '@/assets/Rb/bajaTension2.jpg'
import instalacionRes from '@/assets/Rb/instalacionRes.jpg'
import instalacionRes2 from '@/assets/Rb/instalacionRes2.jpg'
import instalacionIndus from '@/assets/Rb/instalacionIndus.jpg'
import instalacionIndus2 from '@/assets/Rb/instalacionIndus2.jpg'
import tableroDist from '@/assets/Rb/tableroDist.jpg'
import tableroDist2 from '@/assets/Rb/tableroDist2.jpg'
import manejoCircuitos from '@/assets/Rb/manejoCircuitos.jpg'
import manejoCircuitos2 from '@/assets/Rb/manejoCircuitos2.jpg'
import aguaConsumo from '@/assets/Rb/aguaConsumo.jpg'
import aguaConsumo2 from '@/assets/Rb/aguaConsumo2.jpg'
import aguasResiduo from '@/assets/Rb/aguasResiduo.jpg'
import aguasResiduo2 from '@/assets/Rb/aguasResiduo2.jpg'
import calentadorSolar from '@/assets/Rb/calentadorSolar.jpg'
import calentadorSolar2 from '@/assets/Rb/calentadorSolar2.jpg'
import boiler from '@/assets/Rb/boiler.jpeg'
import boiler2 from '@/assets/Rb/boiler2.jpg'
import bombaTinaco from '@/assets/Rb/bombaTinaco.jpg'
import bombaTinaco2 from '@/assets/Rb/bombaTinaco2.jpg'
import anivelamiento from '@/assets/Rb/anivelamiento.jpg'
import anivelamiento2 from '@/assets/Rb/anivelamiento2.jpg'
import consResidencia from '@/assets/Rb/consResidencia.jpg'
import consResidencia2 from '@/assets/Rb/consResidencia2.jpg'
import pisosAzulejos from '@/assets/Rb/pisosAzulejos.jpg'
import pisosAzulejos2 from '@/assets/Rb/pisosAzulejos2.jpg'
import equiposNuevos from '@/assets/Rb/equiposNuevos.jpg'
import equiposNuevos2 from '@/assets/Rb/equiposNuevos2.jpg'
import buenFuncionamiento from '@/assets/Rb/buenFuncionamiento.jpg'
import buenFuncionamiento2 from '@/assets/Rb/buenFuncionamiento2.jpg'
export default {
  created() {
    this.infoActiva.push(this.default),
      this.imagesActivas.push(this.defaultImages)
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
      imagesActivas: [],
      defaultImages: [
        bajaTension,
        bajaTension2,
        instalacionRes,
        instalacionRes2,
        instalacionIndus,
        instalacionIndus2,
        tableroDist,
        tableroDist2,
        manejoCircuitos,
        manejoCircuitos2,
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
          images: [
            bajaTension,
            bajaTension2,
            instalacionRes,
            instalacionRes2,
            instalacionIndus,
            instalacionIndus2,
            tableroDist,
            tableroDist2,
            manejoCircuitos,
            manejoCircuitos2,
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
          images: [
            aguaConsumo,
            aguaConsumo2,
            aguasResiduo,
            aguasResiduo2,
            calentadorSolar,
            calentadorSolar2,
            boiler,
            boiler2,
            bombaTinaco,
            bombaTinaco2,
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
          images: [
            anivelamiento,
            anivelamiento2,
            consResidencia,
            consResidencia2,
            pisosAzulejos,
            pisosAzulejos2,
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
          images: [
            equiposNuevos,
            equiposNuevos2,
            buenFuncionamiento,
            buenFuncionamiento2,
          ],
        },
      ],
    }
  },
  methods: {
    seleccionarServicio(id, info, images) {
      this.servicioActivo = id
      this.infoActiva = []
      this.infoActiva.push(info)
      this.imagesActivas = []
      this.imagesActivas.push(images)
    },
  },
}
</script>

<style lang="scss" scoped>
.cardDesktop {
  height: 494px;
}
</style>
