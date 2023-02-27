<template>
  <div class="q-my-lg">
    <q-card class="my-card">
      <q-card-section>
        <q-form @submit="onSubmit" class="q-gutter-md">
          <q-input outlined dense :type="type" v-model="username"
            :label="`نام کاربری (${type === 'number' ? 'تلفن' : 'ایمیل'})`" error="true"
            :rules="[val => !!val || 'این فیلد الزامی است']" hide-bottom-space>
            <template #append>
              <q-btn-toggle v-model="type" dense flat size="sm" toggle-color="primary" :options="options">
                <template #1>
                  <q-icon name="phone" />
                </template>
                <template #2>
                  <q-icon name="mail" />
                </template>
              </q-btn-toggle>
            </template>
          </q-input>
          <q-input v-model="password" outlined dense label="رمز" :type="isPwd ? 'password' : 'text'">
            <template v-slot:append>
              <q-icon :name="isPwd ? 'visibility_off' : 'visibility'" class="cursor-pointer" @click="isPwd = !isPwd" />
            </template>
          </q-input>
          <q-input v-model="repeatPassword" outlined dense label="تکرار رمز" :type="isPwdRepeat ? 'password' : 'text'">
            <template v-slot:append>
              <q-icon :name="isPwdRepeat ? 'visibility_off' : 'visibility'" class="cursor-pointer"
                @click="isPwdRepeat = !isPwdRepeat" />
            </template>
          </q-input>
          <div>
            <q-btn @mouseover.stop="checkValidation" label="Submit" class="submit-btn" type="submit" color="primary" />
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
const repeatPassword = ref(null);
const type = ref("number");
const isPwd = ref(true);
const isPwdRepeat = ref(true);
const options = ref([
  { label: "", value: "number", slot: 1 },
  { label: "", value: "email", slot: 2 },
]);
const errors = ref(true)
function onSubmit () {
  errors.value = false
}
function checkValidation () {
  setTimeout(() => {
    if (errors.value) {
      let btn = document.querySelector('.submit-btn')
      btn.classList.remove('bg-primary')
      btn.classList.add('bg-red')
      console.log(btn)
    } else {

    }
  }, 10)
}
</script>
<style></style>
