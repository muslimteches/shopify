<template>
  <q-page>
    <!-- content -->
    <div class="row full-width justify-center bg-svg" style="min-height: 100vh">
      <div class="col-6">
        <TopTitle />
        <FormComponent />
      </div>
    </div>
  </q-page>
</template>

<script setup>
import FormComponent from 'src/components/login/FormComponent.vue';
import TopTitle from "src/components/login/TopTitle.vue";
</script>
<style lang="scss">
.bg-svg {
  background-image: url("data:image/svg+xml,%3csvg xmlns='http://www.w3.org/2000/svg' version='1.1' xmlns:xlink='http://www.w3.org/1999/xlink' xmlns:svgjs='http://svgjs.com/svgjs' width='1437' height='558' preserveAspectRatio='none' viewBox='0 0 1437 558'%3e%3cg mask='url(%26quot%3b%23SvgjsMask1005%26quot%3b)' fill='none'%3e%3crect width='1437' height='558' x='0' y='0' fill='%230e2a47'%3e%3c/rect%3e%3cpath d='M 0%2c242 C 95.8%2c209 287.4%2c73 479%2c77 C 670.6%2c81 766.4%2c258.2 958%2c262 C 1149.6%2c265.8 1341.2%2c129.2 1437%2c96L1437 558L0 558z' fill='%2312d9d2'%3e%3c/path%3e%3cpath d='M 0%2c344 C 41.2%2c379 123.6%2c505.8 206%2c519 C 288.4%2c532.2 329.6%2c424.2 412%2c410 C 494.4%2c395.8 535.6%2c458.2 618%2c448 C 700.4%2c437.8 741.6%2c342.6 824%2c359 C 906.4%2c375.4 947.6%2c529.8 1030%2c530 C 1112.4%2c530.2 1154.6%2c364 1236%2c360 C 1317.4%2c356 1396.8%2c480 1437%2c510L1437 558L0 558z' fill='rgba(255%2c 239%2c 224%2c 1)'%3e%3c/path%3e%3c/g%3e%3cdefs%3e%3cmask id='SvgjsMask1005'%3e%3crect width='1437' height='558' fill='white'%3e%3c/rect%3e%3c/mask%3e%3c/defs%3e%3c/svg%3e");
}
</style>
