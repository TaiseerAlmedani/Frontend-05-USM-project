<template>
  <v-navigation-drawer color="primary" dark app permanent>
      <template v-slot:prepend>
        <v-list-item two-line>
          <v-list-item-avatar>
            <img src="@/assets/logo.png">
          </v-list-item-avatar>

          <v-list-item-content>
            <v-list-item-title>USM University</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </template>

      <v-divider></v-divider>

      <v-list
        dense
        nav
      >
        <v-list-item
          v-for="item in items"
          :key="item.title"
          :to="item.link"
          link
          exact
        >
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
</template>

<script>
export default {
  data: () => ({
    items: [
      { title: 'Community', icon: 'mdi-home', link: { name: 'Community' } },
      { title: 'Boards', icon: 'mdi-chart-bar', link: { name: 'Boards' } },
      { title: 'Chat Room', icon: 'mdi-chat' },
      { title: 'Profile', icon: 'mdi-account' },
      { title: 'Search', icon: 'mdi-magnify' },
      { title: 'Settings', icon: 'mdi-cog' },
      { title: 'Login / Sign up', icon: 'mdi-earth' },
    ],
  }),
}
</script>