<template>
    <v-container class="my-15">
        <v-row justify="center">
            <v-col lg="12" class="text-center">
                <v-subheader class="text-h4 justify-center">Portofolio</v-subheader>
                <p>Delectus quaerat obcaecati perferendis eligendi excepturi!</p>
            </v-col>
            <v-col lg="12">
                <div class="text-center">
                    <v-chip @click="activePortfolio = 'webapp'" :color="activePortfolio == 'webapp' ? 'success': ''" class="mx-5">Web App</v-chip>
                    <v-chip @click="activePortfolio = 'mobileapp'" :color="activePortfolio == 'mobileapp' ? 'success': ''" class="mx-5">Mobile App</v-chip>
                    <v-chip @click="activePortfolio = 'desktopapp'" :color="activePortfolio == 'desktopapp' ? 'success': ''" class="mx-5">Desktop App</v-chip>
                </div>
            </v-col>
            <slot v-if="activePortfolio == 'webapp'">
                <v-col lg="3" v-for="(web, webindex) in webApps" :key="webindex">
                    <v-card>
                        <v-img
                            :src="web.image"
                            class="white--text align-end"
                            gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                            height="200px"
                            >
    
                            <v-card-title>{{web.title}}</v-card-title>
                        </v-img>
                    </v-card>
                </v-col>
            </slot>
            <slot v-if="activePortfolio == 'mobileapp'">
                <v-col lg="3" v-for="(mobile, mobileindex) in mobileapp" :key="mobileindex">
                    <v-card>
                        <v-img
                            :src="mobile.image"
                            class="white--text align-end"
                            gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                            height="200px"
                            >
    
                            <v-card-title>{{mobile.title}}</v-card-title>
                        </v-img>
                    </v-card>
                </v-col>
            </slot>
        </v-row>
    </v-container>
</template>

<script>
export default{
    name:'PortofolioItem',
    data(){
        return{
            activePortfolio:'webapp',
            webApps: [
                {title: 'Web apps 1',image:'https://www.tbpc.co/wp-content/uploads/2019/12/travel-portal-img.jpg'},
                {title: 'Web apps 2',image:'https://www.pngitem.com/pimgs/m/15-155460_web-development-mobile-app-development-animation-hd-png.png'},
                {title: 'Web apps 3',image:'https://www.pngitem.com/pimgs/m/127-1272199_custom-web-apps-mobile-app-development-png-transparent.png'},
                {title: 'Web apps 4',image:'https://www.pngitem.com/pimgs/m/127-1272222_web-application-development-png-png-download-web-based.png'},
                {title: 'Web apps 5',image:'https://www.kindpng.com/picc/m/15-155308_mobile-app-development-png-mobile-app-illustrations-png.png'},
                {title: 'Web apps 6',image:'https://www.kindpng.com/picc/m/127-1272131_overview-progressive-web-application-development-web-app-development.png'},
                {title: 'Web apps 7',image:'https://www.kindpng.com/picc/m/127-1272120_web-application-development-ict-month-2018-theme-hd.png'},
                {title: 'Web apps 8',image:'https://www.pngitem.com/pimgs/m/127-1272278_web-application-development-service-hd-png-download.png'}
            ],
            mobileapp:[
                {title: 'mobile apps 1',image:'https://www.tbpc.co/wp-content/uploads/2019/12/travel-portal-img.jpg'},
                {title: 'mobile apps 2',image:'https://www.pngitem.com/pimgs/m/15-155460_mobile-development-mobile-app-development-animation-hd-png.png'},
                {title: 'mobile apps 3',image:'https://www.pngitem.com/pimgs/m/127-1272199_custom-mobile-apps-mobile-app-development-png-transparent.png'},
                {title: 'mobile apps 4',image:'https://www.pngitem.com/pimgs/m/127-1272222_web-application-development-png-png-download-web-based.png'},
            ]
        }
    }
}

</script>