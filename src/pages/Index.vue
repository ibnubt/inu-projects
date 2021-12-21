<template>
  <div class="container">
    <q-carousel
      animated
      v-model="slide"
      arrows
      prev-icon="arrow_left"
      next-icon="arrow_right"
      navigation
      infinite
    >
      <q-carousel-slide :name="1" img-src="https://images-wixmp-ed30a86b8c4ca887773594c2.wixmp.com/f/17945c27-4d87-49e9-87f1-8f09067550bb/ddkm2te-e0869eae-b55f-4e97-967f-a5825172306d.jpg/v1/fill/w_1600,h_500,q_75,strp/lose_control_amv_promo_3_by_lopmonify_ddkm2te-fullview.jpg?token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJ1cm46YXBwOjdlMGQxODg5ODIyNjQzNzNhNWYwZDQxNWVhMGQyNmUwIiwiaXNzIjoidXJuOmFwcDo3ZTBkMTg4OTgyMjY0MzczYTVmMGQ0MTVlYTBkMjZlMCIsIm9iaiI6W1t7InBhdGgiOiJcL2ZcLzE3OTQ1YzI3LTRkODctNDllOS04N2YxLThmMDkwNjc1NTBiYlwvZGRrbTJ0ZS1lMDg2OWVhZS1iNTVmLTRlOTctOTY3Zi1hNTgyNTE3MjMwNmQuanBnIiwiaGVpZ2h0IjoiPD01MDAiLCJ3aWR0aCI6Ijw9MTYwMCJ9XV0sImF1ZCI6WyJ1cm46c2VydmljZTppbWFnZS53YXRlcm1hcmsiXSwid21rIjp7InBhdGgiOiJcL3dtXC8xNzk0NWMyNy00ZDg3LTQ5ZTktODdmMS04ZjA5MDY3NTUwYmJcL2xvcG1vbmlmeS00LnBuZyIsIm9wYWNpdHkiOjk1LCJwcm9wb3J0aW9ucyI6MC40NSwiZ3Jhdml0eSI6ImNlbnRlciJ9fQ.JmQ45W9XGtvg3seQJumDv6D58wz-a6I_tit6ZlOpAFE" />
      <q-carousel-slide :name="2" img-src="https://images-wixmp-ed30a86b8c4ca887773594c2.wixmp.com/f/17945c27-4d87-49e9-87f1-8f09067550bb/ddkm2te-e0869eae-b55f-4e97-967f-a5825172306d.jpg/v1/fill/w_1600,h_500,q_75,strp/lose_control_amv_promo_3_by_lopmonify_ddkm2te-fullview.jpg?token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJ1cm46YXBwOjdlMGQxODg5ODIyNjQzNzNhNWYwZDQxNWVhMGQyNmUwIiwiaXNzIjoidXJuOmFwcDo3ZTBkMTg4OTgyMjY0MzczYTVmMGQ0MTVlYTBkMjZlMCIsIm9iaiI6W1t7InBhdGgiOiJcL2ZcLzE3OTQ1YzI3LTRkODctNDllOS04N2YxLThmMDkwNjc1NTBiYlwvZGRrbTJ0ZS1lMDg2OWVhZS1iNTVmLTRlOTctOTY3Zi1hNTgyNTE3MjMwNmQuanBnIiwiaGVpZ2h0IjoiPD01MDAiLCJ3aWR0aCI6Ijw9MTYwMCJ9XV0sImF1ZCI6WyJ1cm46c2VydmljZTppbWFnZS53YXRlcm1hcmsiXSwid21rIjp7InBhdGgiOiJcL3dtXC8xNzk0NWMyNy00ZDg3LTQ5ZTktODdmMS04ZjA5MDY3NTUwYmJcL2xvcG1vbmlmeS00LnBuZyIsIm9wYWNpdHkiOjk1LCJwcm9wb3J0aW9ucyI6MC40NSwiZ3Jhdml0eSI6ImNlbnRlciJ9fQ.JmQ45W9XGtvg3seQJumDv6D58wz-a6I_tit6ZlOpAFE" />
      <q-carousel-slide :name="3" img-src="https://images-wixmp-ed30a86b8c4ca887773594c2.wixmp.com/f/17945c27-4d87-49e9-87f1-8f09067550bb/ddkm2te-e0869eae-b55f-4e97-967f-a5825172306d.jpg/v1/fill/w_1600,h_500,q_75,strp/lose_control_amv_promo_3_by_lopmonify_ddkm2te-fullview.jpg?token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJ1cm46YXBwOjdlMGQxODg5ODIyNjQzNzNhNWYwZDQxNWVhMGQyNmUwIiwiaXNzIjoidXJuOmFwcDo3ZTBkMTg4OTgyMjY0MzczYTVmMGQ0MTVlYTBkMjZlMCIsIm9iaiI6W1t7InBhdGgiOiJcL2ZcLzE3OTQ1YzI3LTRkODctNDllOS04N2YxLThmMDkwNjc1NTBiYlwvZGRrbTJ0ZS1lMDg2OWVhZS1iNTVmLTRlOTctOTY3Zi1hNTgyNTE3MjMwNmQuanBnIiwiaGVpZ2h0IjoiPD01MDAiLCJ3aWR0aCI6Ijw9MTYwMCJ9XV0sImF1ZCI6WyJ1cm46c2VydmljZTppbWFnZS53YXRlcm1hcmsiXSwid21rIjp7InBhdGgiOiJcL3dtXC8xNzk0NWMyNy00ZDg3LTQ5ZTktODdmMS04ZjA5MDY3NTUwYmJcL2xvcG1vbmlmeS00LnBuZyIsIm9wYWNpdHkiOjk1LCJwcm9wb3J0aW9ucyI6MC40NSwiZ3Jhdml0eSI6ImNlbnRlciJ9fQ.JmQ45W9XGtvg3seQJumDv6D58wz-a6I_tit6ZlOpAFE" />
      <q-carousel-slide :name="4" img-src="https://images-wixmp-ed30a86b8c4ca887773594c2.wixmp.com/f/17945c27-4d87-49e9-87f1-8f09067550bb/ddkm2te-e0869eae-b55f-4e97-967f-a5825172306d.jpg/v1/fill/w_1600,h_500,q_75,strp/lose_control_amv_promo_3_by_lopmonify_ddkm2te-fullview.jpg?token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJ1cm46YXBwOjdlMGQxODg5ODIyNjQzNzNhNWYwZDQxNWVhMGQyNmUwIiwiaXNzIjoidXJuOmFwcDo3ZTBkMTg4OTgyMjY0MzczYTVmMGQ0MTVlYTBkMjZlMCIsIm9iaiI6W1t7InBhdGgiOiJcL2ZcLzE3OTQ1YzI3LTRkODctNDllOS04N2YxLThmMDkwNjc1NTBiYlwvZGRrbTJ0ZS1lMDg2OWVhZS1iNTVmLTRlOTctOTY3Zi1hNTgyNTE3MjMwNmQuanBnIiwiaGVpZ2h0IjoiPD01MDAiLCJ3aWR0aCI6Ijw9MTYwMCJ9XV0sImF1ZCI6WyJ1cm46c2VydmljZTppbWFnZS53YXRlcm1hcmsiXSwid21rIjp7InBhdGgiOiJcL3dtXC8xNzk0NWMyNy00ZDg3LTQ5ZTktODdmMS04ZjA5MDY3NTUwYmJcL2xvcG1vbmlmeS00LnBuZyIsIm9wYWNpdHkiOjk1LCJwcm9wb3J0aW9ucyI6MC40NSwiZ3Jhdml0eSI6ImNlbnRlciJ9fQ.JmQ45W9XGtvg3seQJumDv6D58wz-a6I_tit6ZlOpAFE" />
    </q-carousel>
    <div class="wrapper">
      <!-- <div class="titlenih text-center">
      </div> -->
      <p class="text-overline text-center titlenih" style="font-size: 1.2rem;"><span>Shop Our Products</span></p>
      
      <div class="row justify-between q-col-gutter-lg q-mt-lg q-mb-xl">
        <div class="col-md-3 col-6" v-for="(item, index) in items" :key="'img'+index">
          <div class="card-item">
            <img :src="item.url" class="header-card">
            <p class="q-my-xs text-weight-bolder text-overline">{{item.name}}</p>
            <p>Terbuat dari material berkualitas sehingga awet dan nyaman saat dipakai. Pilihan yang tepat untuk segala macam aktivitas harian anda.</p>
          </div>
        </div>
      </div>

      <p class="text-overline text-center titlenih" style="font-size: 1.2rem;"><span>Our Clients</span></p>
      
      <div class="row justify-between q-col-gutter-lg q-mt-lg">
        <div class="col-md-2 col-2 q-my-auto" v-for="(item, index) in clients" :key="'img'+index">
          <div class="card-item">
            <img :src="item.url" class="size-client">
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { ref } from 'vue'

export default {
  data () {
    return {
      slide: ref(1),
      items: [
        {name: 'PEDOT', url: 'https://d29c1z66frfv6c.cloudfront.net/pub/media/catalog/product/large/7ec4456e6403e2b01a80b2b9d08bfd7df06070f3_xxl-1.jpg', desc: ''},
        {name: 'MBEW', url: 'https://d29c1z66frfv6c.cloudfront.net/pub/media/catalog/product/large/9c9ef076ebfd3250742a1d8c86179f329c20e98e_xxl-1.jpg', desc: ''},
        {name: 'CUDAK', url: 'https://d29c1z66frfv6c.cloudfront.net/pub/media/catalog/product/large/9fdfcc23665fe9e2b389b686a85cc9c97084d238_xxl-1.jpg', desc: ''},
        {name: 'BONGKENG', url: 'https://d29c1z66frfv6c.cloudfront.net/pub/media/catalog/product/large/cdf72617f9ac4426ca28c52f0b99b5d523fc71fe_xxl-1.jpg', desc: ''}
      ],
      clients: [
        {url: 'https://pngimg.com/uploads/car_logo/car_logo_PNG1648.png'},
        {url: 'http://assets.stickpng.com/thumbs/580b57fcd9996e24bc43c46a.png'},
        {url: 'https://freepngimg.com/save/17833-toyota-logo-png-image/370x300'},
        {url: 'https://www.freepnglogos.com/uploads/ford-cars-logo-brands-png-images-15.png'},
        {url: 'https://www.freeiconspng.com/uploads/mercedes-benz-car-logo-brand-png-3.png'},
        {url: 'https://freepngimg.com/thumb/car%20logo/28-audi-car-logo-png-brand-image.png'},
      ]
    }
  }
}
</script>

<style scoped>
.card-item{
  text-align: center;
  cursor: pointer;
}
.card-item:hover .header-card {
  opacity: 0.6;
}
.header-card{
  max-height:300px;
  max-width: 100%;
}
.titlenih {
   width: 100%; 
   text-align: center; 
   border-bottom: 1px solid #000; 
   line-height: 0.1em;
   margin: 10px 0 20px; 
} 
.titlenih span { 
    background:#fff; 
    padding:0 30px; 
}
.size-client{
  width: 100%;
  max-height: 200px;
}
</style>