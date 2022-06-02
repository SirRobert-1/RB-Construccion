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
        <li
          v-for="(info, index) of infoActiva[0]"
          :key="index"
          class="titulo text-center my-10"
        >
          {{ info.servicio }}
          <div class="flex imgContenedor my-2">
            <img
              class="imgServicioDesktop object-cover rounded-xl"
              :src="image"
              alt=""
              v-for="(image, index) of info.images"
              :key="index"
            />
          </div>
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
import bajaTension from '@/assets/Rb/bajaTension.jpg'
import bajaTension2 from '@/assets/Rb/bajaTension2.jpg'
import bajaTension3 from '@/assets/Rb/bajaTension3.jpg'
import instalacionRes from '@/assets/Rb/instalacionRes.jpg'
import instalacionRes2 from '@/assets/Rb/instalacionRes2.jpg'
import instalacionRes3 from '@/assets/Rb/instalacionRes3.jpg'
import instalacionRes4 from '@/assets/Rb/instalacionRes4.jpg'
import instalacionIndus from '@/assets/Rb/instalacionIndus.jpg'
import instalacionIndus2 from '@/assets/Rb/instalacionIndus2.jpg'
import instalacionIndus3 from '@/assets/Rb/instalacionIndus3.jpg'
import instalacionIndus4 from '@/assets/Rb/instalacionIndus4.jpg'
import instalacionIndus5 from '@/assets/Rb/instalacionIndus5.jpg'
import tableroDist from '@/assets/Rb/tableroDist.jpg'
import tableroDist2 from '@/assets/Rb/tableroDist2.jpg'
import manejoCircuitos from '@/assets/Rb/manejoCircuitos.jpg'
import manejoCircuitos2 from '@/assets/Rb/manejoCircuitos2.jpg'
import aguaConsumo from '@/assets/Rb/aguaConsumo.jpg'
import aguaConsumo2 from '@/assets/Rb/aguaConsumo2.jpg'
import aguasResiduo2 from '@/assets/Rb/aguasResiduo2.jpg'
import calentadorSolar from '@/assets/Rb/calentadorSolar.jpg'
import calentadorSolar2 from '@/assets/Rb/calentadorSolar2.jpg'
import boiler from '@/assets/Rb/boiler.jpeg'
import boiler2 from '@/assets/Rb/boiler2.jpg'
import bombaTinaco from '@/assets/Rb/bombaTinaco.jpg'
import anivelamiento from '@/assets/Rb/anivelamiento.jpg'
import anivelamiento2 from '@/assets/Rb/anivelamiento2.jpg'
import anivelamiento3 from '@/assets/Rb/anivelamiento3.jpg'
import remodelacion1 from '@/assets/Rb/remodelacion1.jpg'
import remodelacion2 from '@/assets/Rb/remodelacion2.jpg'
import consResidencia from '@/assets/Rb/consResidencia.jpg'
import consResidencia2 from '@/assets/Rb/consResidencia2.jpg'
import consResidencia3 from '@/assets/Rb/consResidencia3.jpg'
import pisosAzulejos from '@/assets/Rb/pisosAzulejos.jpg'
import pisosAzulejos2 from '@/assets/Rb/pisosAzulejos2.jpg'
import pisosAzulejos3 from '@/assets/Rb/pisosAzulejos3.jpg'
import reparacionSup from '@/assets/Rb/reparacionSup.jpg'
import lijado from '@/assets/Rb/lijado.jpg'
import pintura3 from '@/assets/Rb/pintura3.jpg'
import pintura4 from '@/assets/Rb/pintura4.jpg'
import equiposNuevos from '@/assets/Rb/equiposNuevos.jpg'
import equiposNuevos2 from '@/assets/Rb/equiposNuevos2.jpg'
import buenFuncionamiento from '@/assets/Rb/buenFuncionamiento.jpg'
import buenFuncionamiento2 from '@/assets/Rb/buenFuncionamiento2.jpg'
import aguasResiduo3 from '@/assets/Rb/aguasResiduo3.jpg'
import aguasResiduo4 from '@/assets/Rb/aguasResiduo4.jpg'
import anivelamiento4 from '@/assets/Rb/anivelamiento4.jpg'
import anivelamiento5 from '@/assets/Rb/anivelamiento5.jpg'
import anivelamiento6 from '@/assets/Rb/anivelamiento6.jpg'
import calentadorSolar3 from '@/assets/Rb/calentadorSolar3.jpg'
import consResidencia4 from '@/assets/Rb/consResidencia4.jpg'
import consResidencia5 from '@/assets/Rb/consResidencia5.jpg'
import consResidencia6 from '@/assets/Rb/consResidencia6.jpg'
import consResidencia7 from '@/assets/Rb/consResidencia7.jpg'
import equiposNuevos3 from '@/assets/Rb/equiposNuevos3.jpg'
import equiposNuevos4 from '@/assets/Rb/equiposNuevos4.jpg'
import tableroDist3 from '@/assets/Rb/tableroDist3.jpg'
import hidroPres from '@/assets/Rb/hidroPres.jpg'
import hidroPres1 from '@/assets/Rb/hidroPres1.jpg'
import hidroPres2 from '@/assets/Rb/hidroPres2.jpg'
import hidroPres3 from '@/assets/Rb/hidroPres3.jpg'
import hidroPres4 from '@/assets/Rb/hidroPres4.jpg'
import asfaltico from '@/assets/Rb/asfaltico.jpg'
import imper from '@/assets/Rb/imper.jpg'
import repGrietas from '@/assets/Rb/repGrietas.jpg'
export default {
  created() {
    this.infoActiva.push(this.default)
  },
  data() {
    return {
      servicioActivo: 'electrico',
      infoActiva: [],
      default: [
        {
          servicio: 'Baja tension',
          images: [bajaTension, bajaTension2, bajaTension3],
        },
        {
          servicio: 'Instalación residencial',
          images: [
            instalacionRes,
            instalacionRes2,
            instalacionRes3,
            instalacionRes4,
          ],
        },
        {
          servicio: 'Instalación tipo industrial',
          images: [
            instalacionIndus,
            instalacionIndus2,
            instalacionIndus3,
            instalacionIndus4,
            instalacionIndus5,
          ],
        },
        {
          servicio: 'Tablero de distibución',
          images: [tableroDist, tableroDist2, tableroDist3],
        },
        {
          servicio: 'Conocimiento en manejo de circuitos',
          images: [manejoCircuitos, manejoCircuitos2],
        },
      ],
      imagesActivas: [],

      servicios: [
        {
          id: 'electrico',
          icon: electrica,
          iconW: electricaW,
          titulo: 'Instalación eléctrica',
          info: [
            {
              servicio: 'Baja tension',
              images: [bajaTension, bajaTension2, bajaTension3],
            },
            {
              servicio: 'Instalación residencial',
              images: [
                instalacionRes,
                instalacionRes2,
                instalacionRes3,
                instalacionRes4,
              ],
            },
            {
              servicio: 'Instalación tipo industrial',
              images: [
                instalacionIndus,
                instalacionIndus2,
                instalacionIndus3,
                instalacionIndus4,
                instalacionIndus5,
              ],
            },
            {
              servicio: 'Tablero de distibución',
              images: [tableroDist, tableroDist2, tableroDist3],
            },
            {
              servicio: 'Conocimiento en manejo de circuitos',
              images: [manejoCircuitos, manejoCircuitos2],
            },
          ],
        },
        {
          id: 'hidro',
          icon: hidro,
          iconW: hidroW,
          titulo: 'Instalación hidrosanitaria',
          info: [
            {
              servicio: 'Suministro de agua para consumo',
              images: [aguaConsumo, aguaConsumo2],
            },
            {
              servicio: 'Evacuación de aguas residuales',
              images: [aguasResiduo3, aguasResiduo4],
            },
            {
              servicio: 'Calentador solar',
              images: [calentadorSolar, calentadorSolar2, calentadorSolar3],
            },
            { servicio: 'Mantenimiento a boiler', images: [boiler, boiler2] },
            {
              servicio: 'Bomba-cisterna-tinaco',
              images: [bombaTinaco],
            },
            {
              servicio: 'Hidroneumáticos y presurizador',
              images: [
                hidroPres,
                hidroPres1,
                hidroPres2,
                hidroPres3,
                hidroPres4,
              ],
            },
            { servicio: 'Aguas pluviales', images: [] },
          ],
        },
        {
          id: 'construccion',
          icon: construccion,
          iconW: construccionW,
          titulo: 'Construcción',
          info: [
            {
              servicio: 'Anivelamiento de terreno',
              images: [
                anivelamiento,
                anivelamiento2,
                anivelamiento3,
                anivelamiento4,
                anivelamiento5,
                anivelamiento6,
              ],
            },
            {
              servicio: 'Remodelación y ampliaciones',
              images: [remodelacion1, remodelacion2],
            },
            {
              servicio: 'Construcción residencial',
              images: [
                consResidencia,
                consResidencia2,
                consResidencia3,
                consResidencia4,
                consResidencia5,
                consResidencia6,
                consResidencia7,
              ],
            },
            {
              servicio: 'Colocación de pisos y azulejos',
              images: [pisosAzulejos, pisosAzulejos2, pisosAzulejos3],
            },
          ],
        },
        {
          id: 'pintura',
          icon: pintura,
          iconW: pinturaW,
          titulo: 'Pintura',
          info: [
            { servicio: 'Reparacion de superficies', images: [reparacionSup] },
            { servicio: 'Lijado', images: [lijado] },
            {
              servicio: 'Preparación de colores',
              images: [pintura3, pintura4],
            },
            { servicio: 'Impermeabilización', images: [imper] },
            { servicio: 'Revestimiento de paredes y techos', images: [] },
            { servicio: 'Fibrado y asfáltico', images: [asfaltico] },
            {
              servicio: 'Reparación de grietas y agujeros',
              images: [repGrietas],
            },
          ],
        },
        {
          id: 'aires',
          icon: aires,
          iconW: airesW,
          titulo: 'Aires acondicionados',
          info: [
            {
              servicio: 'Instalación de equipos nuevos',
              images: [
                equiposNuevos,
                equiposNuevos2,
                equiposNuevos3,
                equiposNuevos4,
              ],
            },
            {
              servicio: 'Revisión de buen funcionamiento de A.C.',
              images: [buenFuncionamiento, buenFuncionamiento2],
            },
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

<style lang="scss">
.cardDesktop {
  height: 100%;
  width: 1000px;
}

.titulo {
  font-size: 20px;
}

.imgContenedor {
  max-width: 1000px;
  overflow-x: auto;
}

.imgContenedor::-webkit-scrollbar {
  background-color: #cccccc;
  height: 5px;
  border-radius: 10px;
}
.imgContenedor::-webkit-scrollbar-thumb {
  background-color: #06113c;
  border-radius: 10px;
}

.imgServicioDesktop {
  height: 300px;
  margin: 0rem 1rem 2rem 1rem;
  object-fit: cover;
}
</style>
