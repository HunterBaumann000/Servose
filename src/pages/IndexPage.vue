<template>
    <div class="q-my-xl">  
        <div class="col q-ml-xl">
            <div class="row full-width banner-area justify-start ">
                <div class="banner-content col-lg-5 q-mx-xl">
                    <h1>Servose</h1>
                    
                    <h4 style="margin-top:3em; margin-left: 2em;">Find Services or Become a Service Provider in Minutes!</h4>
                </div>
                <!-- place image stuff here -->
                
            </div>
        </div>
        <div style="margin-top: 8em;"/>
        <div style="padding-bottom: 4em;" class="bg-primary">
        <div style="padding-top:2em" class="row items-center"><div class="col text-center"><h4 class="text-white">Browse Popular Categories</h4></div></div>
        
          <div class="q-pt-sm q-gutter-x-md row items-start justify-center">
          <q-card class="my-card q-my-sm" v-bind:key="item" v-for="item of list" style="width:240px; ">
            <q-img src="https://cdn.quasar.dev/img/parallax2.jpg">
              <div class="absolute-bottom text-subtitle2 text-center">
                Title
              </div>
            </q-img>
          </q-card>
        </div>
            <!-- <search-bar/> -->
        </div>
        <div class="q-ma-xl">
           <h2> Popular Providers</h2>
        </div>
       

        <div style="margin-top: 40em;">
     
        </div>

        <div style="padding-bottom: 60em;" class="bg-primary"></div>

        <div style="margin-top: 40em;">
     
        </div>
        
    </div>
</template>

<script>
import { defineComponent } from 'vue'
import { ref } from 'vue'

export default defineComponent({
  name: 'IndexPage',

  setup () {
    return {
      list: [1, 2, 3,1, 2, 3,1, 2, 3,1, 4, 4],
      stars: ref(2),
      slide: ref(0),
      autoplay: ref(true),
      lorem: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Itaque voluptatem totam, architecto cupiditate officia rerum, error dignissimos praesentium libero ab nemo.'
    }
  }
})
</script>
