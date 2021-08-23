<template>
    <v-container>
        <v-row class="d-flex align-center">
            <v-col
                cols="12"
                md="6"
            >
                <h1>SELAMAT DATANG DI DESA WISATA LESTARI KUMEJING</h1>
                <p>Destinasi wisata penuh sensasi dan dipadukan dengan alam yang sangat eksotis. Hubungi kontak di bawah untuk informasi lebih lanjut dan dapatkan pengalaman berlibur yang menyenangkan sekarang juga!</p>
                <v-row>
                    <v-col cols="auto">
                        <v-btn
                            href="#paket"
                            depressed
                            dark
                        >
                            <span>Lihat Paket</span>
                        </v-btn>
                    </v-col>
                    <v-col cols="auto">
                        <v-btn
                            href="https://maps.google.com/?q=pesonakumejing"
                            target="_blank"
                            outlined
                        >
                            <span class="mr-2">Cari Rute</span>
                            <v-icon>mdi-map-marker</v-icon>
                        </v-btn>
                    </v-col>
                </v-row>
            </v-col>
            <v-col
                cols="12"
                md="6"
            >
                <v-img src="../assets/background.png"/>
            </v-col>
        </v-row>
    </v-container>
</template>