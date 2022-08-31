<template>
    <div class="column items-center">
      <div class="row q-ma-xl">
        <h4 class="text-h4 text-black q-my-md">Sign Into Servose to Find and Host Services</h4>
      </div>
      <div class="row">
        <q-card square bordered class="q-pa-lg shadow-1">
          <q-card-section>
            <q-form class="q-gutter-md">
              <q-input square filled clearable v-model="email" type="email" label="Email" />
              <q-input square filled clearable v-model="password" type="password" label="Password" />
            </q-form>
          </q-card-section>
          <q-card-section class="text-center q-pa-none">
            <p class="text-grey-6">Not Registered? <a href="s"> Create an Account</a></p>
          </q-card-section>
          <q-card-actions class="q-px-md">
            <q-btn unelevated color="primary" size="lg" class="full-width" label="Login"  @click="submit()" />
          </q-card-actions>
          <div class="text-center">OR</div>
          <q-card-actions class="q-px-md">
            <q-btn unelevated color="secondary" size="md" class="full-width" label="Sign in With Google"  @click="submit()" />
          </q-card-actions>
        </q-card>
      </div>
    </div>
</template>




<script>
import { defineComponent } from 'vue'
import { ref } from 'vue'

export default defineComponent({
  name: 'LoginPage',

  data () {
    return {
      email: '',
      password: '',

      submit () {
        this.$router.replace({path: '/', params: true})
      },
      

    }
  }
});
</script>

<style>
.q-card {
  width: 360px;
}
</style>