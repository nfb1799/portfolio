<template>
  <v-app-bar
    id="nav-bar"
    color="black"
  >
    <v-app-bar-title
      :class="platform === 'mobile' ? 'mr-6' : ''"
      :style="platform === 'mobile' ? 'font-size: 1.8em;' : 'text-align: center; font-size: 2em;'"
    >
      Nik Barbero
    </v-app-bar-title>
    <v-spacer v-if="platform !== 'mobile'" />
    <v-btn
      v-if="platform !== 'mobile'"
      style="height: 100%;"
      @click="$router.push({ path: '/' })"
    >
      Home
    </v-btn>
    <v-btn
      v-if="platform !== 'mobile'"
      style="height: 100%;"
      @click="$router.push({ path: '/gallery' })"
    >
      Gallery
    </v-btn>
    <v-btn
      v-if="platform !== 'mobile'"
      style="height: 100%;"
      @click="$router.push({ path: '/resume' })"
    >
      Resume
    </v-btn>
    <v-menu v-if="platform === 'mobile'">
      <template v-slot:activator="{ props }">
        <v-btn
          v-bind="props"
        >
          Menu
        </v-btn>
      </template>
      <v-list>
        <v-list-item class="pa-0">
          <v-btn
            style="height: 100%; width: 100%"
            @click="$router.push({ path: '/' })"
          >
            Home
          </v-btn>
        </v-list-item>
        <v-list-item class="pa-0">
          <v-btn
            style="height: 100%; width: 100%"
            @click="$router.push({ path: '/gallery' })"
          >
            Gallery
          </v-btn>
        </v-list-item>
        <v-list-item class="pa-0">
          <v-btn
            style="height: 100%; width: 100%"
            @click="$router.push({ path: '/resume' })"
          >
            Resume
          </v-btn>
        </v-list-item>
      </v-list>
    </v-menu>
  </v-app-bar>
</template>

<script setup>
import { computed } from 'vue'
import Bowser from 'bowser'

const platform = computed(() => {
  return Bowser.getParser(window.navigator.userAgent).getPlatformType()
})
</script>

<style>
.v-list-item__content {
  height: 100%;
}

/* Custom nav button hover effect */
.v-btn {
  transition: box-shadow 0.18s, background 0.18s, color 0.18s, transform 0.18s;
}
.v-btn:hover, .v-btn:focus-visible {
  box-shadow: 0 4px 16px rgba(0,0,0,0.18);
  transform: translateY(-2px) scale(1.04);
}
</style>