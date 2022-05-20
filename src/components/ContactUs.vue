<template>
    <v-container class="my-15">
        <v-row justify="center">
            <v-col lg="12" class="text-center">
                <v-subheader class="text-h4 justify-center">Contact Us</v-subheader>
                <p>Delectus quaerat obcaecati perferendis eligendi excepturi!</p>
            </v-col>
            <v-col lg="6">
                <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d63368.71518479926!2d107.52744643862017!3d-6.944887115447938!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x2e68ef6cc7ce160f%3A0xfc2a4cc9c815116a!2sHilfi%20Developer!5e0!3m2!1sid!2sid!4v1652926433177!5m2!1sid!2sid" width="100%" height="450" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
            </v-col>
            <v-col lg="6">
                <v-form ref="form">
                    <v-text-field
                        v-model="contactInfo.name"
                        :counter="10"
                        :rules="nameRules"
                        label="Name"
                        required
                    ></v-text-field>

                    <v-text-field
                        v-model="contactInfo.email"
                        :rules="emailRules"
                        label="E-mail"
                        required
                    ></v-text-field>
                    <v-textarea label="Message" v-model="contactInfo.message"></v-textarea>

                    <v-btn color="success" class="mr-4">
                        Send
                    </v-btn>
                </v-form>
            </v-col>
        </v-row>
    </v-container>
</template>


<script>
    export default{
        name: "ContactUs",
        data(){
            return{
                contactInfo:{}
            }
        }
    }

</script>