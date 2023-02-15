<template>
  <div style="padding: 20px">
    <q-card
      flat
      class="my-card"
      style="
        padding: 25px 10px 0;
        background: radial-gradient(circle, #c0d7ee 0%, #c1e9f1 100%);
      "
      ><q-card-section>
        <q-form @submit="onSumbit" class="q-gutter-md">
          <q-input
            filled
            dense
            square
            outlined
            v-model="username"
            label="username"
          />
          <q-input
            v-model="password"
            dense
            filled
            :type="isPwd ? 'password' : 'text'"
            label="password"
          >
            <template v-slot:append>
              <q-icon
                :name="isPwd ? 'visibility_off' : 'visibility'"
                class="cursor-pointer"
                @click="isPwd = !isPwd"
              /> </template
          ></q-input>

          <div>
            <q-btn dense flat label="sumbit" type="sumbit" color="#121212" />
          </div>
        </q-form> </q-card-section
    ></q-card>
  </div>
</template>

<script setup>
import { ref } from "vue";
const isPwd = ref(true);
const username = ref(null);
const password = ref(null);
function onSumbit() {
  alert("sabtnam ok shod");
}
</script>
