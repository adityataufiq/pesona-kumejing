<template>
    <div class="pb-12">
        <v-container>
            <v-col
                cols="12"
                class="text-center"
            >
                <span class="font-weight-bold">Untuk informasi dan reservasi lebih lanjut hubungi:</span>
            </v-col>
            <v-row class="d-flex justify-center">
                <v-col
                    cols="12"
                    md="2"
                    class="text-center"
                    v-for="contact in contacts"
                    :key="contact.title"
                >
                    <v-btn
                        :href="contact.route"
                        target="_blank"
                        outlined
                    >
                        <span class="mr-2">{{ contact.title }}</span>
                        <v-icon>{{ contact.icon }}</v-icon>
                    </v-btn>
                </v-col>
            </v-row>
        </v-container>
    </div>
</template>

<script>
export default {
  data: () => ({
    contacts: [
      {title: 'Kontak Kami', icon: 'mdi-whatsapp', route: 'https://wa.me/6285227161222'},
      {title: 'Instagram', icon: 'mdi-instagram', route: 'https://www.instagram.com/pesonakumejing'},
    ],
  }),
};
</script>