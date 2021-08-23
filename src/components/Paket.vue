<template>
  <div class="py-12">
    <v-container>
      <v-row>
        <v-col cols="12">
          <v-divider></v-divider>
          <h2 class="my-3 text-center">PAKET WISATA</h2>
          <v-divider></v-divider>
        </v-col>
        <v-col
          cols="12"
          md="4"
          class="mx-auto"
          v-for="packet in packets"
          :key="packet.title"
        >
          <v-card
            outlined
          >
            <v-card-title>{{ packet.title }}</v-card-title>
            <v-card-text>
              <span class="font-weight-bold">Fasilitas*</span>
              <ul>
                <li
                  v-for="facility in packet.facilities"
                  :key="facility.name"
                >
                  {{ facility.name }}
                </li>
              </ul>
            </v-card-text>
            <v-card-text>
              <span class="font-weight-bold">Harga</span>
              <ul>
                <li
                  v-for="price in packet.prices"
                  :key="price.item"
                >
                  {{ price.item }}
                </li>
              </ul>
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {
  data: () => ({
    packets: [
      {
        title: 'Paket Satu Hari',
        facilities: [
          {name: 'Transportasi Pulang Pergi'},
          {name: 'Snack'},
          {name: 'Makan 1 Kali'},
          {name: 'Banana Boat'},
        ],
        prices: [
          {item: 'Rp132.000,00/pax (5 - 10 orang)'},
          {item: 'Rp97.000,00/pax (11 - 15 orang)'},
          {item: 'Rp80.000,00/pax (> 15 orang)'},
        ]
      },
      {
        title: 'Paket Satu Hari Satu Malam',
        facilities: [
          {name: 'Transportasi Pulang Pergi'},
          {name: 'Snack'},
          {name: 'Makan 3 Kali'},
          {name: 'Banana Boat'},
          {name: 'Api Unggun'},
          {name: 'Homestay'},
        ],
        prices: [
          {item: 'Rp262.000,00/pax (5 - 10 orang)'},
          {item: 'Rp199.000,00/pax (11 - 15 orang)'},
          {item: 'Rp136.000,00/pax (> 15 orang)'},
        ]
      },
    ]
  }),
};
</script>