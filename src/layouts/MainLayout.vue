<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated class="bg-white">
      <div id="nvbar">
        <div id="nv-main">
          <img src="logos\Logo1.jpg" alt="" id="nv-logo">

          <div id="contactos">
            <div class="nv-nros">
              <img src="icons\llamar.png" alt="">
              <div class="nvn-txt">
                <p>533-4339</p>
                <p>994-428-965</p>
              </div>
            </div>
            <div class="nv-nros">
              <img src="icons\llamar.png" alt="">
              <div class="nvn-txt">
                <p>99653-3223</p>
                <p>937-514-867</p>
              </div>
            </div>
            <div class="nv-nros">
              <img src="icons\correo.png" alt="">
              <div class="nvn-txt">
                <p>netperu100@hotmail.com</p>
              </div>
            </div>
            <div class="nv-nros">
              <img src="icons\mapa.png" alt="">
              <div class="nvn-txt">
                <p>Lima, PERÚ</p>
              </div>
            </div>
            <div class="nv-nros">
              <img src="icons\cisco-gif.gif" alt="" id="cisco-gif">
            </div>
          </div>

          <input type="text" placeholder="Buscar..." id="searchbar">
        </div>

        <div id="nv-2">
          <a href="" class="nv2-types">
            <img src="icons\catalyst.png" alt="">
            <p>Switch Catalyst</p>
          </a>
          <a href="" class="nv2-types">
            <img src="icons\Cisco Business.ico" alt="">
            <p>Cisco Business</p>
          </a>
          <a href="" class="nv2-types">
            <img src="icons\Switch Industrial.ico" alt="">
            <p>Switch Industrial</p>
          </a>
          <a href="" class="nv2-types">
            <img src="icons\rt.png" alt="">
            <p>Aironet</p>
          </a>
          <a href="" class="nv2-types">
            <img src="icons\Télefono.ico" alt="">
            <p>Teléfono</p>
          </a>
          <a href="" class="nv2-types">
            <img src="icons\mariakii.ico" alt="">
            <p>Meraki</p>
          </a>
          <a href="" class="nv2-types">
            <img src="icons\Transceiver.ico" alt="">
            <p>Transceiver</p>
          </a>
        </div>

        <!-- <div id="nv-3">
          <q-breadcrumbs class="text-brown">
            <template v-slot:separator>
              <q-icon size="1.5vw" name="chevron_right" color="primary" />
            </template>

<q-breadcrumbs-el label="Home" icon="home" to="/" />
<q-breadcrumbs-el label="MIKROTIK" icon="widgets" to="/" />
<q-breadcrumbs-el label="RouterB" icon="router" to="/" />
<q-breadcrumbs-el label="RB750" icon="broadcast_on_personal" />
</q-breadcrumbs>
</div> -->

      </div>
    </q-header>



    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import { defineComponent } from 'vue'


export default defineComponent({
  name: 'MainLayout',

  components: {

  },

  setup() {

    return {

    }
  }
})
</script>

<style lang="scss" scoped>
#nvbar {
  display: flex;
  flex-direction: column;
  color: black;
  padding: 0 4vw;

  #nv-main {
    display: flex;
    flex-direction: row;
    align-content: center;
    justify-content: space-between;
    align-items: center;
    padding: 0.5vw 0;

    #nv-logo {
      width: 8vw;
    }

    #contactos {
      display: flex;
      flex-direction: row;
      justify-content: center;
      align-items: center;
      align-content: center;
      gap: 2vw;

      .nv-nros {
        display: flex;
        flex-direction: row;
        gap: 0.5vw;
        align-items: center;
        justify-content: center;
        justify-items: center;
        // border: 1px solid red;

        img {
          width: 2vw;
        }

        .nvn-txt {
          display: flex;
          flex-direction: column;
          // border: 1px solid red;
          align-content: center;
          justify-content: center;
          margin: 0;
          padding: 0;

          p {
            margin: 0;
            padding: 0;
            font-weight: bolder;
            font-size: 1vw;
          }
        }

        #cisco-gif {
          width: 6vw;
        }
      }
    }

    #searchbar {
      width: 20vw;
      height: 3vw;
      background: url('icons/lupa.png') no-repeat scroll 7px 7px;
      padding-left: 3vw;
      background-size: 1.5vw;
      background-position: 1vw;
      border: grey solid 0.1vw;
      border-radius: 2vw;
      font-size: 1vw;
      transition: 0.2s all;

      &::placeholder {
        font-size: 1vw;
        align-self: center;
      }

      &:focus {
        outline: none;
        border: $primary solid 0.2vw;
      }
    }
  }

  #nv-2 {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-content: center;
    border-top: 0.1vw solid rgba(128, 128, 128, 0.505);
    padding: 0.5vw 0;

    a {
      display: flex;
      flex-direction: row;
      justify-content: center;
      align-content: center;
      align-items: center;
      text-decoration: none;
      width: 10vw;

      img {
        width: 1.5vw;
        margin-right: 0.2vw;
      }

      p {
        all: unset;
        font-size: 1vw;
        color: black;
        transition: 0.2s all;
      }


      &:hover {
        p {
          color: $primary;
          font-weight: bold;
        }
      }
    }
  }

  #nv-3 {
    border-top: 0.1vw solid rgba(128, 128, 128, 0.505);
    padding: 0.5vw 0;

    font-size: 1vw;
  }
}
</style>
