<template>
<app-header @button-selete="type"/>
  <main class="main">
    <div class="sub-content">
      <component :is="isSelete"/>
    </div>
  </main>
</template>

<script>
import AllBox from "@/components/qrcode/AllBox.vue";
import QrCreate from "@/components/qrcode/QrCreate.vue";
import QrSkan from "@/components/qrcode/QrSkan.vue";
import AppHeader from "@/components/AppHeader.vue";
import {ref,computed} from "vue";
export default {
  name: 'App',
  components: {
    AppHeader,
    AllBox,
    QrCreate,
    QrSkan,
  },
  setup() {
    const property = ref("All");
    const type = (t) => {
      property.value = t;
    }
    const isSelete = computed(() => {
      let name;
      switch (property.value) {
        case "All":
          name = "AllBox";
          break;
        case "Skan":
          name = "QrSkan";
          break;
        case "Create":
          name = "QrCreate";
          break;
      }
      return name;
    });

    return  {
      type,
      isSelete,
    }
  }
}
</script>
<style>
</style>
