<template>
    <div class="flex flex-col min-h-screen font-Roboto bg-weather-primary">
      <SiteNavigation />
      <RouterView v-slot="{Component}">
        <Transtion name="page" mode="out-in">
          <component :is="Component"/>
        </Transtion>
      </RouterView>
    </div>
</template>

<script setup >
import {RouterView} from "vue-router"
import SiteNavigation from "./components/SiteNavigation.vue";
</script>
<style  scoped>

.page-enter-active,
.page-leave-active{
  transition: 600ms ease all;
}

.page-enter-from,
.page-leave-to{
  opacity: 0;
}


</style>