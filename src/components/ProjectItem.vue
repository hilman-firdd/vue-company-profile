<template>
    <v-container class="my-15">
        <v-row justify="center">
            <v-col lg="12" class="text-center">
                <v-subheader class="text-h4 justify-center">Project</v-subheader>
                <p>Delectus quaerat obcaecati perferendis eligendi excepturi!</p>
            </v-col>
            <v-col lg="4" v-for="project in 3" :key="project">
                <v-card
                    class="mx-auto my-12"
                    max-width="374"
                >
                <v-img
                    height="250"
                    src="https://amesyn.com/wp-content/uploads/2020/12/web-application-development.png"
                    >
                </v-img>
                <v-card-title>Web Development</v-card-title>
                <v-card-text>
                    <div>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Itaque veniam officiis quam laudantium reiciendis voluptates, dicta incidunt voluptas mollitia. Temporibus excepturi, consectetur voluptas eveniet laborum porro architecto? Sint, iure aspernatur.</div>
                </v-card-text>
                <v-divider class="mx-4"></v-divider>
                <v-card-actions>
                    <v-btn color="success" rounded>View Details</v-btn>
                    <v-spacer/>
                    <v-rating
                        :value="4.5"
                        color="amber"
                        dense
                        half-increments
                        readonly
                        size="14">
                    </v-rating>
                </v-card-actions>
                </v-card>
            </v-col>
        </v-row>
    </v-container>
</template>