<template>
  <div>
    <q-card class="my-card"><q-card-section>    <q-form @submit="onSumbit"  class="q-gutter-md">
     </div> <q-input square outlined v-model="username" label="square outlined" />
      <q-input square outlined v-model="password" label="square outlined" />
      <div>
        <q-btn label="sumbit" type="sumbit" color="primary" />
       
      </div>
    </q-form>
    </q-card-section></q-card>
  </div>
</template>

<script setup>
import { ref } from "vue";
const username = ref(null);
const password = ref(null);
function onSumbit() {
  alert("sabtnam ok shod");
}
</script>
