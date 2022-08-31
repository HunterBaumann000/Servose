<template> 
    <div class="row">
        <div class="col-2">
            <div class="" style="max-width: 350px">
                <q-list bordered padding>
                <q-item-label header>Favorites</q-item-label>

                <q-item clickable v-ripple>
                    <q-item-section>
                    <q-item-label>Content filtering</q-item-label>
                    <q-item-label caption>
                        Set the content filtering level to restrict
                        apps that can be downloaded
                    </q-item-label>
                    </q-item-section>
                </q-item>

                <q-item clickable v-ripple>
                    <q-item-section>
                    <q-item-label>Random Word</q-item-label>
                    <q-item-label caption>
                        Require password for purchase or use
                        password to restrict purchase
                    </q-item-label>
                    </q-item-section>
                </q-item>

                <q-separator spaced />
                <q-item-label header>General</q-item-label>

                <q-item tag="label" v-ripple>
                    <q-item-section side top>
                    <q-checkbox v-model="check1" />
                    </q-item-section>

                    <q-item-section>
                    <q-item-label>Words Here</q-item-label>
                    <q-item-label caption>
                        Notify me about updates to apps or games
                    </q-item-label>
                    </q-item-section>
                </q-item>

                <q-item tag="label" v-ripple>
                    <q-item-section side top>
                    <q-checkbox v-model="check2" />
                    </q-item-section>

                    <q-item-section>
                    <q-item-label>Sound</q-item-label>
                    <q-item-label caption>
                        Auto-update at anytime. Data charges may apply
                    </q-item-label>
                    </q-item-section>
                </q-item>

                <q-item tag="label" v-ripple>
                    <q-item-section side top>
                    <q-checkbox v-model="check3" />
                    </q-item-section>

                    <q-item-section>
                    <q-item-label>Alotta Stuff</q-item-label>
                    <q-item-label caption>
                        Automatically add home screen stuff
                    </q-item-label>
                    </q-item-section>
                </q-item>

                <q-separator spaced />
                <q-item-label header>Adv Filters</q-item-label>

                <q-item tag="label" v-ripple>
                    <q-item-section>
                    <q-item-label>switch 1</q-item-label>
                    </q-item-section>
                    <q-item-section side >
                    <q-toggle color="blue" v-model="notif1" val="battery" />
                    </q-item-section>
                </q-item>

                <q-item tag="label" v-ripple>
                    <q-item-section>
                    <q-item-label>Switch 2</q-item-label>
                    <q-item-label caption>Allow notification</q-item-label>
                    </q-item-section>
                    <q-item-section side top>
                    <q-toggle color="green" v-model="notif2" val="friend" />
                    </q-item-section>
                </q-item>

                <q-item tag="label" v-ripple>
                    <q-item-section>
                    <q-item-label>Rand Switch 3</q-item-label>
                    <q-item-label caption>Allow notification when uploading images</q-item-label>
                    </q-item-section>
                    <q-item-section side top>
                    <q-toggle color="red" v-model="notif3" val="picture" />
                    </q-item-section>
                </q-item>

                <q-separator spaced />
                <q-item-label header>Other settings</q-item-label>
                </q-list>
            </div>
        </div>

        <div class="col-8 q-mx-xl">  
            <h4>Browse Categories</h4>
        </div>

        <div class="col-4">

        </div>
    </div>
</template>

<script>
import { defineComponent } from 'vue'
import { ref } from 'vue'

export default defineComponent({
  name: 'ExplorePage',
  components: {
  },

  data () {
    return {
      email: '',
      password: ''
    }
  }
})
</script>

<style>
.q-card {
  width: 360px;
}
</style>