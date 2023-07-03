<script setup>
import { QrStream } from 'vue3-qr-reader'
const onDecode = (result) => {
  console.log("result===>",result);
}
</script>

<template>
  <qr-stream @decode="onDecode" class="mb">
    <div style="color: red;" class="frame"></div>
  </qr-stream>
</template>

<style scoped>

</style>