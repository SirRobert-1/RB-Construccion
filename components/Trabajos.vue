<template>
  <section class="trabajos text-blue bg-blue w-screen px-10 pt-36">
    <card-Servicios
      v-for="(servicio, index) of servicios"
      :key="index"
      :icon="servicio.icon"
      :titulo="servicio.titulo"
      :info="servicio.info"
      :images="servicio.images"
    />
  </section>
</template>
<script>
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
import aguaConsumo2 from '@/assets/Rb/aguaConsumo.jpg'
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
  data() {
    return {
      servicios: [
        {
          icon: electrica,
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
          icon: hidro,
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
          icon: construccion,
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
          icon: pintura,
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
          icon: aires,
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
}
</script>
