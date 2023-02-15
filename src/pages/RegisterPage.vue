<template>
  <q-page>
    <!-- content -->
    <div class="row full-width justify-center" style="min-height: 100vh">
      <div class="col-6">
        <TopTitlee />
        <FormComponent />
      </div>
    </div>
  </q-page>
</template>

<script setup>
import FormComponent from "src/components/login/FormComponent.vue";
import TopTitle from "src/components/login/TopTitle.vue";
</script>
