<template>
  <div>
    <q-card class="my-card bg-backdrop">
      <q-card-section>
        <q-form @submit="onSubmit" class="q-gutter-md">
          <q-input
            outlined
            dense
            clearable
            v-model="username"
            :label="`نام کاربری (${type === 'number' ? 'تلفن' : 'ایمیل'})`"
            :rules="[(val) => (!!val && val.length >= 3) || 'لطفا خالی نذارید']"
            hide-bottom-space
          />
          <template #append>
            <q-btn-toggle
              v-model="type"
              dense
              size="sm"
              toggle-color="primary"
              :options="options"
            >
              <template #1> <q-icon name="phone" /> </template>
              <template #2>
                <q-icon name="mail" />
              </template>
            </q-btn-toggle>
          </template>

          <q-input
            v-model="password"
            outlined
            dense
            clearable
            label="رمز عبور"
            :type="isPwd ? 'password' : 'text'"
            :rules="[(val) => val.length >= 8 || 'لطفا از 8 کاراکتر کم نباشد']"
            hide-bottom-space
          >
            <template v-slot:append>
              <q-icon
                :name="isPwd ? 'visibility_off' : 'visibility'"
                class="cursor-pointer"
                @click="isPwd = !isPwd"
              />
            </template>
          </q-input>
          <q-input
            v-model="repeatPassword"
            outlined
            dense
            clearable
            label="تکرار رمز"
            :type="isPwdRepeat ? 'password' : 'text'"
            :rules="[(val) => val.length >= 8 || 'لطفا از 8 کاراکتر کم نباشد']"
            hide-bottom-space
          >
            <template v-slot:append>
              <q-icon
                :name="isPwdRepeat ? 'visibility_off' : 'visibility'"
                class="cursor-pointer"
                @click="isPwdRepeat = !isPwdRepeat"
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
const repeatPassword = ref(null);
const ispwd = ref(true);
const isPwdRepeat = ref(true);
const type = ref("number");
const options = ref([
  { label: "", value: "number", slot: 1 },
  { label: "", value: "email", slot: 2 },
]);
function onSubmit() {}
</script>
<style lang="scss">
.bg-backdrop {
  backdrop-filter: blur(10px);
}
/* Chrome, Safari, Edge, Opera */
input::-webkit-outer-spin-button,
input::-webkit-inner-spin-button {
  -webkit-appearance: none;
  margin: 0;
}

/* Firefox */
input[type="number"] {
  -moz-appearance: textfield;
}
</style>
