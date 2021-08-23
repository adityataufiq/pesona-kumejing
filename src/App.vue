<template>
  <v-app>
    <v-app-bar
      app
      color="white"
    >
      <div class="d-flex align-center">
        <v-img
          alt="Logo Kumejing"
          class="shrink mr-2"
          contain
          src="./assets/logo-kumejing.png"
          transition="scale-transition"
          width="40"
        />
      </div>

      <v-spacer></v-spacer>

      <div
        class="hidden-sm-and-down"
        v-for="nav in navs"
        :key="nav.title"
      >
        <v-btn
          :href="nav.route"
          text
        >
          <span class="mr-2">{{ nav.title }}</span>
        </v-btn>
      </div>
    </v-app-bar>

    <v-main>
      <router-view/>
    </v-main>
  </v-app>
</template>

<script>

export default {
  name: 'App',

  data: () => ({
    navs: [
      {title: 'beranda', route: '#beranda'},
      {title: 'tentang', route: '#tentang'},
      {title: 'fasilitas', route: '#fasilitas'},
      {title: 'paket', route: '#paket'},
      {title: 'kontak', route: '#kontak'},
    ]
  }),
};
</script>
