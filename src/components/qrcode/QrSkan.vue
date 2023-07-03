<script setup>
import { QrcodeStream } from 'vue-qrcode-reader'
const onDecode = (result) => {
  console.log(result);
}
</script>

<template>
  <div>
    <qrcode-stream @onDecode="onDecode" />
  </div>
</template>

<style scoped>

</style>