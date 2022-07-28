<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated>
      <q-toolbar>
        <q-btn
          flat
          dense
          round
          icon="menu"
          aria-label="Menu"
          @click="toggleLeftDrawer"
        />

        <q-toolbar-title class="text-weight-bold">
          <span class="gt-sm"> {{$route.name}}</span>
        </q-toolbar-title>
      </q-toolbar>
    </q-header>

    <q-drawer
      show-if-above
      v-model="left"
      side="left"
      :width="283"
      bordered>
      <q-icon
        class="q-pa-md"
        name="fas fa-dove"
        size="lg"
        color="primary"
      />
<q-list>
      <q-item clickable v-ripple>
        <q-item-section avatar>
          <q-avatar color="white" text-color="primary" icon="home" size="lg" />
        </q-item-section>
        <q-item-section class="text-h6">Acceuil</q-item-section>
      </q-item>
  <q-item
    to="/about"
    v-ripple
    clickable
    >
    <q-item-section avatar>
      <q-avatar color="white" text-color="primary" icon="info" size="lg" />
    </q-item-section>
    <q-item-section class="text-h6">A propos</q-item-section>
  </q-item>
</q-list>
    </q-drawer>

    <q-drawer show-if-above v-model="right" side="right" bordered>
      <q-input
        placeholder ="Rechercher"
        class="q-ma-md"
        outlined
        rounded
        dense
        >
        <template v-slot:prepend>
          <q-icon name="search"/>
        </template>
      </q-input>
      <q-list
        separator
        padding
      >
        <q-item class="q-pa-md">
          <q-item-section>
            <q-item-label overline class="text-grey">Education</q-item-label>
            <q-item-label class="text-weight-bold">Super!</q-item-label>
            <q-item-label caption>Secondary line text. Lorem ipsum dolor sit amet, consectetur adipiscit elit.</q-item-label>
          </q-item-section>

          <q-item-section side top>
            <q-item-label caption>5 min ago</q-item-label>
          </q-item-section>
        </q-item>

        <q-item class="q-pa-md">
          <q-item-section>
            <q-item-label overline class="text-grey">Education</q-item-label>
            <q-item-label class="text-weight-bold">Super!</q-item-label>
            <q-item-label caption>Secondary line text. Lorem ipsum dolor sit amet, consectetur adipiscit elit.</q-item-label>
          </q-item-section>

          <q-item-section side top>
            <q-item-label caption>5 min ago</q-item-label>
          </q-item-section>

        </q-item>

        <q-item class="q-pa-md">
          <q-item-section>
            <q-item-label overline class="text-grey">Education</q-item-label>
            <q-item-label class="text-weight-bold">Super!</q-item-label>
            <q-item-label caption>Secondary line text. Lorem ipsum dolor sit amet, consectetur adipiscit elit.</q-item-label>
          </q-item-section>

          <q-item-section side top>
            <q-item-label caption>5 min ago</q-item-label>
          </q-item-section>

        </q-item>
      </q-list>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue';

/*const linksList = [
  {
    title: 'Docs',
    caption: 'quasar.dev',
    icon: 'school',
    link: 'https://quasar.dev'
  },
  {
    title: 'Github',
    caption: 'github.com/quasarframework',
    icon: 'code',
    link: 'https://github.com/quasarframework'
  },
  {
    title: 'Discord Chat Channel',
    caption: 'chat.quasar.dev',
    icon: 'chat',
    link: 'https://chat.quasar.dev'
  },
  {
    title: 'Forum',
    caption: 'forum.quasar.dev',
    icon: 'record_voice_over',
    link: 'https://forum.quasar.dev'
  },
  {
    title: 'Twitter',
    caption: '@quasarframework',
    icon: 'rss_feed',
    link: 'https://twitter.quasar.dev'
  },
  {
    title: 'Facebook',
    caption: '@QuasarFramework',
    icon: 'public',
    link: 'https://facebook.quasar.dev'
  },
  {
    title: 'Quasar Awesome',
    caption: 'Community Quasar projects',
    icon: 'favorite',
    link: 'https://awesome.quasar.dev'
  }
];*/

export default defineComponent({
  name: 'MainLayout',

  components: {

  },

  setup () {
    const leftDrawerOpen = ref(false)

    return {
      leftDrawerOpen,
      toggleLeftDrawer () {
        leftDrawerOpen.value = !leftDrawerOpen.value
      }
    }
  }
});
</script>
