<template>
    <v-container class="myskills">
        <h1 class="text-center">Skills</h1>
        <v-row class="justify-center text-center">
            <v-col
                cols="12"
                lg="4"
                v-for="a in skills"
                :key="a"
                class="content ma-2"
            >
                <div>
                    <v-icon>
                        {{ a.logo }}
                    </v-icon>
                    <h3>{{ a.name }}</h3>
                </div>
            </v-col>
        </v-row>
    </v-container>
</template>

<script>
export default {
    name: 'MySkills',

    data: () => ({
        skills: [
            {
                logo: 'mdi-xml',
                name: 'FrontEnd Engineering'
            },
            {
                logo: 'mdi-account-voice',
                name: 'Digital Marketing'
            },
            {
                logo: 'mdi-account-group',
                name: 'Community Involvement'
            },
            {
                logo: 'mdi-palette',
                name: 'Graphic Design'
            },
            {
                logo: 'mdi-account-search',
                name: 'UI/UX'
            },
            {
                logo: 'mdi-account-multiple-check',
                name: 'Management'
            },
        ]
    })
}
</script>

<style scoped>
    .myskills {
        background-color: var(--primary-color);
    }
    .content {
        border-style: solid;
        border-width: 2px;
        border-color: var(--third-color);
        max-width: 30%;
    }

    @media screen and (max-width: 991px) {
        .content {
            padding: 0;
        }
    }

</style>