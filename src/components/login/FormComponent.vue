<template>
  <div>
    <q-card class="bg-backDrop" flat>
      <q-card-section>
        <q-form @submit="onSubmit" class="q-gutter-md">
          <q-input
            dense
            v-model="username"
            label="نام کاربری (شماره تلفن یا ایمیل)"
          />
          <q-input dense v-model="password" label="رمز عبور" />
          <div>
            <q-btn label="Submit" type="submit" color="primary" />
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
function onSubmit() {
  alert("تمام دوغون");
}
</script>

<style lang="scss">
.bg-backDrop {
  background-color: rgba(0, 0, 0, 0.107);
  backdrop-filter: blur(7px) !important;
  border: 1px solid white;
}
</style>
