<template>
  <b-container class="bv-example-row">
    <h2 style="font-family: 'Bangers', cursive;">Productos</h2><br>
    <b-row>
      <b-col>
        <div @mouseover="hover1 = true" @mouseleave="hover1 = false">
          <transition name="fade">
          <b-card
            v-if="!hover1"
            title="Dualshock 4"
            img-src="https://i.linio.com/p/a3e19d1fd139e0b9151c8183b86f5223-zoom.jpg"
            img-alt="Image"
            img-top
            tag="article"
            style="max-width: 20rem; font-family: 'Bangers', cursive;"
            class="mb-2"
          >
            <b-card-text style="font-family: 'Hind', sans-serif;">El control inalámbrico DualShock®4 para la consola PlayStation®4 define esta generación de juego al combinar funciones revoluc</b-card-text>
            <b-button href="#" variant="primary">Comprar</b-button>
          </b-card>

          <b-card
            v-if="hover1"
            title="Dualshock 4"
            img-src="https://mundoinnovos.com/wp-content/uploads/2018/05/CPS4C3.jpg"
            img-alt="Image"
            img-top
            tag="article"
            style="max-width: 20rem; font-family: 'Bangers', cursive;"
            class="mb-2"
          >
            <b-card-text style="font-family: 'Hind', sans-serif;">El control inalámbrico DualShock®4 para la consola PlayStation®4</b-card-text>
            <b-button href="#" variant="primary">Comprar</b-button>
          </b-card>
          </transition>
        </div>
      </b-col>
      <b-col>
        <div @mouseover="hover2 = true" @mouseleave="hover2 = false">
          <transition name="fade">
          <b-card
          v-if="!hover2"
            title="Silla Gamer"
            img-src="https://www.gamersx.cl/image/cache/catalog/SEVENWIN/SILLAS/CONQUEST/Conquest-Red_1-500x500.png"
            img-alt="Image"
            img-top
            tag="article"
            style="max-width: 20rem; font-family: 'Bangers', cursive;"
            class="mb-2"
          >
            <b-card-text style="font-family: 'Hind', sans-serif;">
              Material del asiento: Espuma Cloruro de polivinilo (PVC)
              Material del respaldo: Espuma Cloruro de polivinilo (PVC)
              Material del marco: Acero inoxidable
            </b-card-text>

            <b-button href="#" variant="primary">Comprar</b-button>
          </b-card>

          <b-card
          v-if="hover2"
            title="Silla Gamer"
            img-src="https://r.btcdn.co/r/eyJzaG9wX2lkIjozNTI2LCJnIjoiMTAwMHgifQ/d2e0a32ec170e1a/523485-1503151-1.jpg"
            img-alt="Image"
            img-top
            tag="article"
            style="max-width: 20rem; font-family: 'Bangers', cursive;"
            class="mb-2"
          >
            <b-card-text style="font-family: 'Hind', sans-serif;">
              Material del asiento: Espuma Cloruro de polivinilo (PVC)
              Material del respaldo: Espuma Cloruro de polivinilo (PVC)
              Material del marco: Acero inoxidable
            </b-card-text>

            <b-button href="#" variant="primary">Comprar</b-button>
          </b-card>
          </transition>
        </div>
      </b-col>
      <b-col>
        <div @mouseover="hover3 = true" @mouseleave="hover3 = false">
          <transition name="fade">
          <b-card
          v-if="!hover3"
            title="Headset"
            img-src="https://dojiw2m9tvv09.cloudfront.net/24346/product/11335942-14644199974511607420.jpg"
            img-alt="Image"
            img-top
            tag="article"
            style="max-width: 20rem; font-family: 'Bangers', cursive;"
            class="mb-2"
          >
            <b-card-text style="font-family: 'Hind', sans-serif;">Con un diseño ultra cómodo y dos micrófonos integrados, el wireless headset gold para PS4 y PS VR te permite descubrir lo bien que suenan tus juegos.</b-card-text>

            <b-button href="#" variant="primary">Comprar</b-button>
          </b-card>

          <b-card
          v-if="hover3"
            title="Headset"
            img-src="https://mod-center.com/6037-large_default/comprar-sony-wireless-stereo-headset-20-ps3-ps4-psvita-negro-barato-ps4-accesorios-oferta-mod-center.jpg"
            img-alt="Image"
            img-top
            tag="article"
            style="max-width: 20rem; font-family: 'Bangers', cursive;"
            class="mb-2"
          >
            <b-card-text style="font-family: 'Hind', sans-serif;">Con un diseño ultra cómodo y dos micrófonos integrados, el wireless headset gold para PS4 y PS VR te permite descubrir lo bien que suenan tus juegos.</b-card-text>

            <b-button href="#" variant="primary">Comprar</b-button>
          </b-card>
          </transition>
        </div>
      </b-col>
    </b-row>
    <hr>
  </b-container>
</template>

<script>
export default {
  data () {
    return {
      hover1: false,
      hover2: false,
      hover3: false
    }
  }
}
</script>

<style scoped>
.bv-example-row {
  margin-top: 20px;
}
.fade-enter-active, .fade-leave-active {
  transition: opacity 5s
}
.fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
  opacity: 1
}
</style>
