<template>
  <v-app dark>
    <Header />
    <v-main id="content">
      <Nuxt />
    </v-main>
    <v-footer dark padless app>
      <v-col class="text-center" cols="12">
        {{ new Date().getFullYear() }} — <strong>nmsohn</strong>
      </v-col>
    </v-footer>
  </v-app>
</template>

<style lang="scss" scoped>
footer {
  position: relative;
}
#content {  
  background: transparent;
  display: contents;
}
</style>
