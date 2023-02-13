<template>
  <div>
    <q-card class="my-card">
      <q-card-section>
        <q-form @submit="onSubmit" class="q-gutter-md">
          <q-input square outlined v-model="username" label="Square outlined" />
          <q-input square outlined v-model="password" label="Square outlined" />
          <div>
            <q-btn label="Submit" type="submit" color="primary" />
          </div>
        </q-form>
      </q-card-section>
    </q-card>


  </div>
</template>

<script setup>
import { ref } from 'vue';
const username = ref(null)
const password = ref(null)
function onSubmit () {
  alert('sabtenam ok shod')
}
</script>
