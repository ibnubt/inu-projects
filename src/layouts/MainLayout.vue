<template>
  <q-layout view="lhh lpr lff">
    <q-header class="navnih" elevated>
      <q-toolbar>
        <q-toolbar-title>
          <div class="row">
              <q-btn
                class="lt-md"
                flat
                dense
                round
                @click="leftDrawerOpen = !leftDrawerOpen"
                icon="menu"
                aria-label="Menu"
              ></q-btn>
              <q-img class="resp-logo" src="../assets/cd.png" style="width: 75px"></q-img>
              <q-img class="gt-sm " src="../assets/cd2.png" style="width: 250px"></q-img>
          </div>
        </q-toolbar-title>

        <div class="gt-sm">
          <q-btn flat label="Home"></q-btn>
          <q-btn flat label="About"></q-btn>
          <q-btn flat label="Product" @mouseover="hello = true"></q-btn>
            <q-menu v-model="hello" @mouseleave="hello = false"  fit>
            <q-list style="width: 100">
              <div class="row">
                <div class="col-6">
                  <q-item>
                    <q-item-section><b class="q-my-xs"><i class="fas fa-tshirt"></i> Brand New Flannel</b></q-item-section>
                  </q-item>
                  <q-item clickable>
                    <q-item-section>Ada Pedot Disini</q-item-section>
                  </q-item>
                  <q-item clickable>
                    <q-item-section>Ada Mbew Disini</q-item-section>
                  </q-item>
                  <q-item clickable>
                    <q-item-section>Ada Cudak Disini</q-item-section>
                  </q-item>
                  <q-item clickable>
                    <q-item-section>Ada Bongkeng Disini</q-item-section>
                  </q-item>
                </div>
                <div class="col-6">
                  <q-item>
                    <q-item-section><b class="q-my-xs"><i class="fas fa-vest-patches"></i> Brand New Hoodie</b></q-item-section>
                  </q-item>
                  <q-item clickable>
                    <q-item-section>Ada Adit Disini</q-item-section>
                  </q-item>
                  <q-item clickable>
                    <q-item-section>Ada Reja Disini</q-item-section>
                  </q-item>
                  <q-item clickable>
                    <q-item-section>Ada Yana Disini</q-item-section>
                  </q-item>
                  <q-item clickable>
                    <q-item-section>Ada Saleh Disini</q-item-section>
                  </q-item>
                </div>
              </div> 
            </q-list>
          </q-menu>
          <q-btn flat label="Contract"></q-btn>
          <q-btn flat label="SIGN IN"></q-btn>
        </div>
        
      </q-toolbar>
    </q-header>
    <q-drawer
      v-model="leftDrawerOpen"
      bordered
    >
      <q-list>
        <q-item-label
          header
        >
          QONTOLODON
        </q-item-label>
        
        <q-btn class="full-width" flat color="primary" label="Memek" />
      </q-list>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
    
    <q-layout-footer>
      <div class="footernih">
        <div class="row">
          <div class="col-12 col-md-5 resp-footer-text">
              <q-img class="resp-logo" src="../assets/cd.png" style="width: 75px"></q-img>
              <q-img src="../assets/cd2.png" style="width: 200px"></q-img>
              <br>
              <p class="q-mt-lg">The Biggest, The Myth, The Legend, The Best Apparel in the World. There's more than 437 Stores accross Indonesia includes Bandung, Jakarta, Tasikmalaya, Garut, Sumedang, etc.</p>
          </div>
          <div class="col-12 col-md-1 q-pt-md resp-footer-text">
            <p class="text-overline title-font">Help</p>
            <label class="pointer">Contact Us</label><br>
            <label class="pointer">Order</label><br>
            <label class="pointer">Career</label><br>
            <label class="pointer">How to Buy</label>
          </div>
          <div class="col-12 col-md-3 q-pt-md resp-footer-text">
            <p class="text-overline title-font">Info</p>
            <label><i class="fas fa-envelope"></i> college.dropout@gmail.com</label><br>
            <label><i class="fas fa-phone-square"></i> 14045</label><br>
            <label><i class="fas fa-map-marker-alt"></i> Jl. Telekomunikasi No. 1, Terusan Buahbatu - Bojongsoang, Sukapura, Kec. Dayeuhkolot, Kabupaten Bandung, Jawa Barat 40257</label>
          </div>
          <div class="col-12 col-md-3 q-pt-md text-center">
            <q-btn class="q-mr-xs" round color="black"><i class="fab fa-instagram"></i></q-btn>
            <q-btn class="q-mr-xs" round color="black"><i class="fab fa-facebook"></i></q-btn>
            <q-btn class="q-mr-xs" round color="black"><i class="fab fa-youtube"></i></q-btn>
            <q-btn class="q-mr-xs" round color="black"><i class="fab fa-tiktok"></i></q-btn>
          </div>
        </div> 
      </div> 
      <div class="footer-edge full-width">2021 © Inu Gaminxksnxsnkx</div>
    </q-layout-footer>
    
  </q-layout>
</template>

<script lang="ts">

import { defineComponent, ref } from 'vue'

export default defineComponent({
  name: 'MainLayout',

  components: {
  },
  data(){
    return{
      hello: false,
    }
  },
  setup () {
    const leftDrawerOpen = ref(false)

    return {
      leftDrawerOpen,
      toggleLeftDrawer () {
        leftDrawerOpen.value = !leftDrawerOpen.value
      }
    }
  }
})
</script>

<style scoped>
@media only screen and (max-width: 1000px) {
  .resp-logo{
      margin-left: auto;
      margin-right: auto;
  }
  .resp-footer-text{
    text-align: center;
  }
}
.navnih {
  color: black;
  background-color: #f7f7f7;
}
.footernih{
  padding: 24px 12%;
  background-color: #f7f7f7;
  text-align: left;
  color: black;
}
.footer-edge{
  background-color: #f7f7f7;
  text-align: center;
}
.q-page-container{
  background: white;
}
.pointer:hover{
  font-weight: bold;
}
</style>