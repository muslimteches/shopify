<template>
  <div>
    <q-card class="my-card" bg-backDrop>
      <q-card-section>
        <q-form @submit="onSubmit" class="q-gutter-md">
          <q-input
            dense
            rounded
            v-model="username"
            label="نام و نام خانوادگی"
          />
          <q-input
            dense
            rounded
            class="cursor-pointer"
            @click="ispwd"
            v-model="password"
            label="رمز عبور"
            hint="Password with toggle"
          />
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
<style lang="scss">
.bg-backDrop {
  backdrop-filter: blur 10px;
}
</style>
