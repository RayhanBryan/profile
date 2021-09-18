<template>
    <v-container class="jumbotron">
        <v-row class="text-center">
            <v-col 
                cols="12"
                lg="6"
            >
                <div class="text-profile">
                    <h1>Rayhan Rizqi Bebryan</h1>
                    <v-row>
                        <v-col
                            sm="12"
                        >
                            <p>Yogyakarta</p>
                        </v-col>
                    </v-row>
                    <v-row class="text-center justify-center">
                        <v-col
                            cols="1"
                        >

                            <v-icon
                                @click='wa'
                            >
                                mdi-whatsapp
                            </v-icon>
                        </v-col>
                        <v-col
                            cols="1"
                        >
                            <v-icon
                                @click='mail'
                            >
                                mdi-email
                            </v-icon>
                        </v-col>
                        <v-col
                            cols="1"
                        >

                            <v-icon
                                @click='linkedin'
                            >
                                mdi-linkedin
                            </v-icon>
                        </v-col>
                        <v-col
                            cols="1"
                        >

                            <v-icon
                                @click='ig'
                            >
                                mdi-instagram
                            </v-icon>
                        </v-col>
                        <v-col
                            cols="1"
                        >

                            <v-icon
                                @click='github'
                            >
                                mdi-github
                            </v-icon>
                        </v-col>
                    </v-row>
                    <v-row class="justify-center">
                        <v-col
                            v-for="a in interest"
                            :key="a"
                            lg="2"
                            cols="12"
                            class="interest"
                        >
                        {{ a }}
                        </v-col>
                    </v-row>
                </div>
            </v-col>

            <v-col
                cols="12"
                lg="6"
            >
                <v-row class="justify-center">
                    <img
                        src="../assets/img/profile.jpeg"
                    >
                </v-row>
            </v-col>
        </v-row>
    </v-container>
</template>

<style scoped>
    .jumbotron{
        background-color: var(--primary-color);
        height: 500px;
    }
    .text-profile{
        margin-top: 30%;
    }
    h1{
        font-weight: 300;
    }
    p{
        margin-bottom: -20px;
    }
    img {
        position: relative;
        top: 40px;
        border-radius: 10px;
        height: 250px;
    }
    @media screen and (min-width: 991px){
        img{
            position: absolute;
            top: 50px;
            height: 500px;
            border-radius: 20px;
        }
    }
    @media screen and (max-width: 991px) {
        .interest {
            display: none;
        }
        .text-profile {
            margin-top: 10%;
        }        
    }
</style>

<script>
export default {
    name: 'TheJumbotron',

    data: () => ({
        interest: [
            'FrontEnd Engineering',
            'UI/UX',
            'Digital Marketing',
            'Chess',
            'Manchester United'
        ]
    }),
    methods: {
        wa () {
            window.open("https://api.whatsapp.com/send?phone=6282138455387", '_blank')
        },
        mail () {
            window.open("mailto:rayhan.r.b@mail.ugm.ac.id", '_blank')
        },
        linkedin () {
            window.open("https://www.linkedin.com/in/rayhanrb/", '_blank')
        },
        ig () {
            window.open("https://www.instagram.com/rayhanbryan/", '_blank')
        },
        github () {
            window.open("https://github.com/RayhanBryan?tab=repositories", '_blank')
        }
    }
}
</script>