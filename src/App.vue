<template>
  <v-app>
    <v-app-bar
      app
      color="#A6B1E1"
      dark
    >
      <div class="d-flex align-center">
        <v-img
          alt="Vuetify Logo"
          class="shrink mr-2"
          contain
          src="https://cdn.vuetifyjs.com/images/logos/vuetify-logo-dark.png"
          transition="scale-transition"
          width="40"
        />

        <v-img
          alt="Vuetify Name"
          class="shrink mt-1 hidden-sm-and-down"
          contain
          min-width="100"
          src="https://cdn.vuetifyjs.com/images/logos/vuetify-name-dark.png"
          width="100"
        />
      </div>

      <v-spacer></v-spacer>

      <v-btn
        v-for="a in subs"
        :key="a"
        v-scroll-to="{ element:a.tag, offset: -60}"
        text
      >
        <span class="mr-2">{{ a.title }}</span>
      </v-btn>
    </v-app-bar>

    <v-main>
      <router-view/>
    </v-main>

  <v-footer
    dark
    padless
  >
    <v-card
      class="flex"
      flat
      tile
    >
      <v-card-title class="footer">
        <h5 class="subheading">Get connected with me on social networks!</h5>

        <v-spacer></v-spacer>

        <v-btn
          v-for="a in icons"
          :key="a"
          class="mx-4"
          dark
          icon
          :href= a.link
          target="_blank"
        >
          <v-icon
            size="24px">
            {{ a.icon }}
          </v-icon>
        </v-btn>
      </v-card-title>

      <v-card-text class="py-2 white--text text-center">
        {{ new Date().getFullYear() }} — <strong>Rayhan Rizqi Bebryan</strong>
      </v-card-text>
    </v-card>
  </v-footer>

  </v-app>
</template>

<style>
  :root {
    --primary-color: #F4EEFF;
    --secondary-color: #DCD6F7;
    --third-color: #A6B1E1;
    --fourth-color: #424874;
  }
  h1 {
    color: var(--fourth-color);
  }
  p{
    padding-bottom: -100px;
  }
  .footer{
    background-color: var(--third-color);
    border-top-left-radius: 20px;
  }
</style>

<script>

export default {
  name: 'App',

  data: () => ({
    subs: [
      {
        tag: '#we',
        title: 'Work Experiences'
      },
      {
        tag: '#edu',
        title: 'Education'
      },
      {
        tag: '#skills',
        title: 'Skills'
      }
    ],
    icons: [
      {
        icon: 'mdi-whatsapp',
        link: "https://api.whatsapp.com/send?phone=6282138455387"
      },
      {
        icon: 'mdi-email',
        link: "mailto:rayhan.r.b@mail.ugm.ac.id"
      },
      {
        icon: 'mdi-linkedin',
        link: "https://www.linkedin.com/in/rayhanrb/"
      },
      {
        icon: 'mdi-instagram',
        link:  "https://www.instagram.com/rayhanbryan/"
      },
      {
        icon: 'mdi-github',
        link: "https://github.com/RayhanBryan?tab=repositories" 
      },
      ],
  }),
};
</script>
