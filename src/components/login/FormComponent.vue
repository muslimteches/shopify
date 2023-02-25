<template>
  <div>
    <q-card class="my-card">
      <q-card-section>
        <q-form @submit="onSubmit" class="q-gutter-md">
          <q-input dense v-model="username" label="نام و نام خانوادگی" />
          <q-input
            v-model="password"
            dense
            label="رمز عبور"
            :type="isPwd ? 'password' : 'text'"
          >
            <template v-slot:append>
              <q-icon
                :name="isPwd ? 'visibility_off' : 'visibility'"
                class="cursor-pointer"
                @click="isPwd = !isPwd"
              />
            </template>
          </q-input>
          <div>
            <q-btn type="submit " color="primary" label="تایید" />
          </div>
        </q-form>
      </q-card-section>
    </q-card>
  </div>
</template>

<script setup>
import { ref } from "vue";
const username = ref(null);
const password = ref(null);
const ispwd = ref(true);
function onSubmit() {}
</script>
<style lang="scss"></style>
