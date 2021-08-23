<template>
  <div class="py-12 grey lighten-4">
    <v-container>
      <v-row>
        <v-col cols="12">
          <v-divider></v-divider>
          <h2 class="my-3 text-center">FASILITAS</h2>
          <v-divider></v-divider>
        </v-col>
        <v-col
          cols="12"
          md="3"
          v-for="facility in facilities"
          :key="facility.title"
        >
          <v-card
            flat
            color="grey lighten-4"
            class="text-center"
          >
            <v-avatar size="100">
              <img
                :src="require(`../assets/${facility.ava}.jpg`)"
                :alt="facility.title"
              >
            </v-avatar>
            <v-card-actions>
              <v-dialog
                v-model="dialog"
                max-width="500"
                scrollable
              >
                <template v-slot:activator="{ on, attrs }">
                  <v-btn
                    depressed
                    class="mx-auto"
                    v-bind="attrs"
                    v-on="on"
                  >
                    <span>{{ facility.title }}</span>
                  </v-btn>
                </template>

                <v-card>
                  <v-card-title>{{ facility.title }}</v-card-title>
                  <v-divider></v-divider>
                  <img
                    :src="require(`../assets/${facility.img}.jpg`)"
                    :alt="facility.title"
                    class="pa-6"
                  >
                  <v-card-text class="text-justify">{{ facility.desc }}</v-card-text>
                  <v-divider></v-divider>
                </v-card>
              </v-dialog>
            </v-card-actions>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {
  data: () => ({
    facilities: [
      {title: 'Banana Boat', ava: 'banana-boat-cropped', img: 'banana-boat', desc: 'Kumejing Banana Boat adalah sebuah permainan atraksi wahana air menggunakan perahu karet yang berbentuk pisang dengan ukuran yang besar dan dapat digunakan untuk 5 hingga 6 penumpang. Banana Boat akan ditarik menggunakan Speedboat selama 15 menit dengan kelengkapan keamanan yang sudah disediakan.'},
      {title: 'Camping Ground', ava: 'camp-ground-cropped', img: 'camp-ground', desc: 'Pesona Kumejing menyediakan sebuah lahan hijau dengan pemandangan Waduk Wadaslintang yang dapat digunakan pengunjung untuk bermalam menggunakan tenda ataupun untuk kegiatan camping sekalipun.'},
      {title: 'Kuliner Bucu Pendem', ava: 'bucu-pendem-cropped', img: 'bucu-pendem', desc: 'Bucu Pendem merupakan kuliner khas Desa Kumejing yang terbuat dari nasi yang dibentuk mengerucut dan berisi ayam utuh (ingkung) di dalam nasinya. Bucu Pendem selalu disajikan di dalam acara-acara besar yang ada di Desa Kumejing seperti ritual malam satu suro.'},
      {title: 'Meeting Outdoor', ava: 'meeting-outdoor-cropped', img: 'meeting-outdoor', desc: 'Outdoor Meeting Room adalah salah satu fasilitas yang ditawarkan Pesona Kumejing. Konsep ruang rapat yang berada di luar membuat suasana menjadi berbeda, karena tidak dibatasi oleh sekat-sekat pada ruangan seperti pada umumnya.'},
    ],
  }),
};
</script>