<template>
    <v-container>
        <h1 class="text-center">Education</h1>
        <v-row class="justify-center text-center">
            <v-col
                v-for="a in edu"
                :key="a"
                lg="6"
            >
            <h2>{{ a.name }}</h2>
            <img :src="require(`../assets/img/edu/` + a.img)" alt="">
            <br>
            {{ a.major }}
            <br>
            {{ a.year }}
            </v-col>
        </v-row>
    </v-container>
</template>

<script>
export default {
    name: 'EduExp',

    data: () => ({
        edu: [
            {
                name: 'Universitas Gadjah Mada',
                img: 'ugm.png',
                major: 'Computer Science',
                year: '2017'
            },
            {
                name: 'Universitas Terbuka',
                img: 'ut.png',
                major: 'Management',
                year: '2018'
            },
        ]
    })

}
</script>

<style scoped>
    img {
        height: 150px;
    }
</style>