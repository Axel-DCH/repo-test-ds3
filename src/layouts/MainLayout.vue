<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated class="bg-white">
      <div id="nvbar" v-if="!isMobileView">
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

      <div id="nbar-m" v-if="isMobileView">
        <q-header elevated class="bg-white text-black">
          <q-toolbar>
            <q-btn flat dense round icon="menu" aria-label="Menu" @click="toggleLeftDrawer" />

            <q-toolbar-title>
              <img src="logos\Logo1.jpg" alt="Logo" style="height: 40px; margin-top: 5px;">
            </q-toolbar-title>

            <q-btn flat dense round icon="search" aria-label="Search" @click="showSearchBar = !showSearchBar" />
          </q-toolbar>

          <q-toolbar v-if="showSearchBar" class="bg-grey-2">
            <q-input dense outlined v-model="searchQuery" placeholder="Buscar..." class="full-width">
              <template v-slot:append>
                <q-icon name="search" />
              </template>
            </q-input>
          </q-toolbar>
        </q-header>

        <q-drawer v-model="leftDrawerOpen" show-if-above bordered class="bg-grey-1">
          <q-list>
            <q-item-label header>
              Categorías
            </q-item-label>

            <q-item clickable v-ripple to="/">
              <q-item-section avatar>
                <img src="icons\catalyst.png" alt="" style="width: 24px; height: 24px;">
              </q-item-section>
              <q-item-section>
                <q-item-label>Switch Catalyst</q-item-label>
              </q-item-section>
            </q-item>
            <q-item clickable v-ripple to="/">
              <q-item-section avatar>
                <img src="icons\Cisco Business.ico" alt="" style="width: 24px; height: 24px;">
              </q-item-section>
              <q-item-section>
                <q-item-label>Cisco Business</q-item-label>
              </q-item-section>
            </q-item>
            <q-item clickable v-ripple to="/">
              <q-item-section avatar>
                <img src="icons\Switch Industrial.ico" alt="" style="width: 24px; height: 24px;">
              </q-item-section>
              <q-item-section>
                <q-item-label>Switch Industrial</q-item-label>
              </q-item-section>
            </q-item>
            <q-item clickable v-ripple to="/">
              <q-item-section avatar>
                <img src="icons\rt.png" alt="" style="width: 24px; height: 24px;">
              </q-item-section>
              <q-item-section>
                <q-item-label>Aironet</q-item-label>
              </q-item-section>
            </q-item>
            <q-item clickable v-ripple to="/">
              <q-item-section avatar>
                <img src="icons\Télefono.ico" alt="" style="width: 24px; height: 24px;">
              </q-item-section>
              <q-item-section>
                <q-item-label>Teléfono</q-item-label>
              </q-item-section>
            </q-item>
            <q-item clickable v-ripple to="/">
              <q-item-section avatar>
                <img src="icons\mariakii.ico" alt="" style="width: 24px; height: 24px;">
              </q-item-section>
              <q-item-section>
                <q-item-label>Meraki</q-item-label>
              </q-item-section>
            </q-item>
            <q-item clickable v-ripple to="/">
              <q-item-section avatar>
                <img src="icons\Transceiver.ico" alt="" style="width: 24px; height: 24px;">
              </q-item-section>
              <q-item-section>
                <q-item-label>Transceiver</q-item-label>
              </q-item-section>
            </q-item>


            <q-separator />

            <q-item-label header>
              Contactos
            </q-item-label>

            <q-item>
              <q-item-section avatar>
                <q-icon name="call" />
              </q-item-section>
              <q-item-section>
                <q-item-label>533-4339</q-item-label>
                <q-item-label caption>994-428-965</q-item-label>
              </q-item-section>
            </q-item>
            <q-item>
              <q-item-section avatar>
                <q-icon name="call" />
              </q-item-section>
              <q-item-section>
                <q-item-label>99653-3223</q-item-label>
                <q-item-label caption>937-514-867</q-item-label>
              </q-item-section>
            </q-item>
            <q-item>
              <q-item-section avatar>
                <q-icon name="email" />
              </q-item-section>
              <q-item-section>
                <q-item-label>netperu100@hotmail.com</q-item-label>
              </q-item-section>
            </q-item>
            <q-item>
              <q-item-section avatar>
                <q-icon name="location_on" />
              </q-item-section>
              <q-item-section>
                <q-item-label>Lima, PERÚ</q-item-label>
              </q-item-section>
            </q-item>
            <q-item>
              <q-item-section avatar>
                <img src="icons\cisco-gif.gif" alt="Cisco" style="width: 40px; height: 40px;">
              </q-item-section>
              <q-item-section>
                <q-item-label>Certificado Cisco</q-item-label>
              </q-item-section>
            </q-item>
          </q-list>
        </q-drawer>
      </div>
    </q-header>



    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import { defineComponent, ref, onMounted, onUnmounted } from 'vue'

export default defineComponent({
  name: 'MainLayout',

  components: {

  },

  setup() {
    const leftDrawerOpen = ref(false)
    const showSearchBar = ref(false)
    const searchQuery = ref('')
    const isMobileView = ref(false)

    const mobileBreakpoint = 768;

    const updateView = () => {
      isMobileView.value = window.innerWidth < mobileBreakpoint;
      if (!isMobileView.value && leftDrawerOpen.value) {
        leftDrawerOpen.value = false;
      }
    };

    onMounted(() => {
      updateView();
      window.addEventListener('resize', updateView);
    });

    onUnmounted(() => {
      window.removeEventListener('resize', updateView);
    });

    return {
      leftDrawerOpen,
      toggleLeftDrawer() {
        leftDrawerOpen.value = !leftDrawerOpen.value
      },
      showSearchBar,
      searchQuery,
      isMobileView
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
