<template>
  <q-page>
    components: { TopTitle },page>
    <!-- content -->
    <div class="row full-width" style="min-height: 100vh">
      <div class="col-6">
        <TopTitle />
      </div>
      <div class="col-6">
        <sideImage />
      </div>
    </div>
  </q-page>
</template>

<script setup>
import sideImage from "src/components/login/SideImage.vue";
import TopTitle from "src/components/login/TopTitle.vue";
</script>
