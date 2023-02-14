<template>
  <q-page>
    <!-- content -->
    <div class="row full-width justify-center bg-svg" style="min-height: 100vh">
      <div class="col-6">
        <TopTitle />
      </div>
    </div>
  </q-page>
</template>

<script setup>
import TopTitle from "src/components/login/TopTitle.vue";
</script>
<style lang="scss">
.bg-svg {
  background-color: #ffefe0;
  background-image: url("deta:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/s'");
  background-attachment: fixed;
  background-size: cover;
}
</style>
