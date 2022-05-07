<template>
  <section class="trabajos text-blue bg-blue w-screen px-10 pt-36">
    <card-Servicios
      v-for="(servicio, index) of servicios"
      :key="index"
      :icon="servicio.icon"
      :titulo="servicio.titulo"
      :info="servicio.info"
    />
  </section>
</template>
<script>
import electrica from '@/assets/electricidad.svg'
import hidro from '@/assets/fontaneria.svg'
import construccion from '@/assets/construccion.svg'
import pintura from '@/assets/pintura.svg'
import aires from '@/assets/aires.svg'
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
        },
      ],
    }
  },
}
</script>
