<template>
    <v-container class="workexp">
        <h1 class="text-center">Work Experiences</h1>
        <v-row class="justify-center text-center">
            <v-col
                v-for="a in we"
                :key="a"
                md="3"
                class="content"
            >
                <h2>{{ a.company }}</h2>
                <img :src="require('../assets/img/we/' + a.img)" alt="">
                <h3>{{ a.position }}</h3>
                <p>{{ a.status }}</p>
                <p>{{ a.year }}</p>
            </v-col>
        </v-row>
    </v-container>
</template>

<style scoped>
    .workexp {
        background-color: var(--primary-color);
        border-top-left-radius: 100px;
        border-bottom-right-radius: 100px;
    }
    img {
        height: 150px;
        border-radius: 50%;
    }
    .content {
        color: var(--third-color);
    }
</style>

<script>
export default {
    name: 'WorkExp',

    data: () => ({
        we: [
            {
                company: 'Nekara',
                img: 'nekara.png',
                position: 'Digital Marketing & Web Dev',
                status: 'Fulltime',
                year: 'July 2021 - September 2021'
            },
            {
                company: 'Eksperia',
                img: 'eksperia.png',
                position: 'Digital Marketing',
                status: 'Intern',
                year: 'July 2021 - Present'
            },
            {
                company: 'Pottani',
                img: 'pottani.png',
                position: 'UI/UX Designer',
                status: 'Fulltime',
                year: 'September 2020 - March 2021'
            },
            {
                company: 'DPKM UGM',
                img: 'dpkm.png',
                position: 'Data Enumerator',
                status: 'Parttime',
                year: 'July 2020 - November 2020'
            },
        ]
    })
}
</script>