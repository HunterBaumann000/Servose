<template>
  <div class="q-pa-md" style="max-width: 800px">

    <q-form
      @submit="onSubmit"
      @reset="onReset"
      class="q-gutter-md"
    >
    <div class="row">
        <div class="col">
            <q-input
            filled
            v-model="name"
            label="Search for Services"
            hint="View Categories"
            lazy-rules
            :rules="[ val => val && val.length > 0 || 'Please type something']"
        />
        </div>
        
        <div class="col">
            <div>
                <!-- <q-btn type="submit" color="primary" icon-search></q-btn> -->
            </div>
        </div>

    </div>

    </q-form>

  </div>
</template>

<script>

import { defineComponent } from 'vue'

export default defineComponent({
  name: "SearchBar",
  setup () {
  }
});
</script>



