<template>
  <q-layout >
    <q-header reveal class="bg-primary text-white">
      <q-toolbar class="row">
        <q-spacer class="col-6 col-md-2"></q-spacer>
        
        <router-link style="text-decoration: none; color: inherit;" to="/">
          <q-toolbar-title>
            
            <q-avatar>
              <img src="https://cdn.quasar.dev/logo-v2/svg/logo-mono-white.svg">
            </q-avatar>
            Servose
          </q-toolbar-title>
        </router-link>
        <q-space />

        <q-tabs v-model="tab" shrink>
        
          <router-link style="text-decoration: none; color: inherit;" to="/explore"><q-tab stretch flat name="tab1" label="Explore Services"/></router-link>
          <router-link style="text-decoration: none; color: inherit;" to="/about"><q-tab stretch flat name="tab2" label="How Servose Works"/></router-link>
          <router-link style="text-decoration: none; color: inherit;" to="/login"><q-tab stretch v-if="!isLoggedIn" flat name="tab4" label="Sign In"/>
            <q-btn-dropdown v-if="isLoggedIn" else="isLoggedIn" stretch flat label="My Account">
              <q-list>
                <q-item-label header>Folders</q-item-label>
                <q-item v-for="n in 3" :key="`x.${n}`" clickable v-close-popup tabindex="0">
                  <q-item-section avatar>
                    <q-avatar icon="folder" color="secondary" text-color="white" />
                  </q-item-section>
                  <q-item-section>
                    <q-item-label>Photos</q-item-label>
                    <q-item-label caption>February 22, 2016</q-item-label>
                  </q-item-section>
                  <q-item-section side>
                    <q-icon name="info" />
                  </q-item-section>
                </q-item>
                <q-separator inset spaced />
                <q-item-label header>Files</q-item-label>
                <q-item v-for="n in 2" :key="`y.${n}`" clickable v-close-popup tabindex="0">
                  <q-item-section avatar>
                    <q-avatar icon="assignment" color="primary" text-color="white" />
                  </q-item-section>
                  <q-item-section>
                    <q-item-label>Vacation</q-item-label>
                    <q-item-label caption>February 22, 2016</q-item-label>
                  </q-item-section>
                  <q-item-section side>
                    <q-icon name="info" />
                  </q-item-section>
                </q-item>
              </q-list>
            </q-btn-dropdown> 
          <q-tab name="tab5" v-if="isLoggedIn">
          <q-avatar rounded>
            <img src="https://cdn.quasar.dev/img/avatar.png">
          </q-avatar>
          </q-tab>
          </router-link>
        </q-tabs>

        <q-spacer class="col-6 col-md-2"></q-spacer>
      </q-toolbar>
    </q-header>

    <q-page-container justify-center>
      <!-- <div class="row" >
        <div class="col-6 col-md-2"></div>
        <div class="col-6 col-md-8"> -->
          <div>
            <router-view /> 
          </div>
        <!-- </div>
        <div class="col-6 col-md-2"></div>
      </div> -->
    </q-page-container>

      <q-footer elevated class="bg-primary">
          <div class="row" >
            <div class="col-1 col-md-2"></div>
            <div class="col-1 col-md-8">
              <div>
                <q-toolbar>
                  <q-toolbar-title></q-toolbar-title>
                </q-toolbar>
              </div>
            </div>
            <div class="col-1 col-md-2"></div>
          </div>
      </q-footer>

  </q-layout>
</template>

<script>
import { defineComponent, ref } from 'vue'


export default defineComponent({
    name: 'MainLayout',

    components: {
      //EssentialLink
    }, 
    data () {
      return {
        isLoggedIn: false,
      }
    }
  }
)
</script>
