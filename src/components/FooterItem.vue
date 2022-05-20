<template>
    <v-footer padless>
        <v-col lg="12">
            <v-row justify="center">
                <v-col lg="4" class="text-center">
                    <v-toolbar-title>Web Hilfideveloper</v-toolbar-title>
                    <v-card-text>
                        <v-btn
                        v-for="icon in icons"
                        :key="icon"
                        class="mx-4 dark--text"
                        icon
                        >
                            <v-icon size="24px">
                                {{ icon }}
                            </v-icon>
                        </v-btn>
                    </v-card-text>
                    <v-subheader>Lorem ipsum dolor sit amet consectetur adipisicing elit. Omnis similique tempore neque blanditiis, facilis illum, velit ad sed eaque placeat natus exercitationem, quasi ex aliquid sapiente? Laudantium consectetur numquam tenetur?</v-subheader>
                    <v-form class="mt-4">
                        <v-text-field label="Email" outlined dense></v-text-field>
                        <v-btn rounded color="success">Subscribe Us</v-btn>
                    </v-form>
                </v-col>
            </v-row>
                <div class="mt-10">
                    <v-divider></v-divider>
                    <v-subheader>
                        Lorem, ipsum dolor sit amet consectetur adipisicing elit. Eaque, quis! {{ new Date().getFullYear() }} — <strong>Vuetify</strong>
                        <v-spacer/>
                        <strong>Design hilman</strong>
                    </v-subheader>
                </div>
        </v-col>
    </v-footer>

</template>

<script>
export default{
    name: "FooterItem",
    data() {
        return {
            icons: [
                'mdi-facebook',
                'mdi-twitter',
                'mdi-linkedin',
                'mdi-instagram',
            ]
        }
    }
}
</script>