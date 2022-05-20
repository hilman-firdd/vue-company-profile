<template>
    <v-container class="my-15">
        <v-row justify="center">
            <v-col lg="12" class="text-center">
                <v-subheader class="text-h4 justify-center">Gallery</v-subheader>
                <p>Delectus quaerat obcaecati perferendis eligendi excepturi!</p>
            </v-col>
            <v-col
                v-for="n in 9"
                :key="n"
                class="d-flex child-flex"
                cols="4"
                lg="3"
                >
                <v-img
                    :src="`https://www.pngitem.com/pimgs/m/140-1405253_free-website-template-one-image-hd-png-download.png`"
                    :lazy-src="`https://www.pngitem.com/pimgs/m/140-1405253_free-website-template-one-image-hd-png-download.png`"
                    aspect-ratio="1"
                    class="grey lighten-2"
                >
                
                </v-img>

            </v-col>
        </v-row>
    </v-container>
</template>
