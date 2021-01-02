<template>
  <div>
    <v-app-bar>
      <v-toolbar-title>ML</v-toolbar-title>

      <v-spacer></v-spacer>

      <span class="hidden-sm-and-up">
        <v-btn @click.stop="drawer = !drawer">Menu</v-btn>
      </span>

      <v-toolbar-items class="hidden-xs-only">
        <v-btn v-for="item in items" :key="item.title" :to="item.link"
          >{{ item.title }}
        </v-btn>
      </v-toolbar-items>
    </v-app-bar>

    <v-navigation-drawer v-model="drawer" absolute temporary right>
      <v-list>
        <v-list-item v-for="item in items" :key="item.title" :to="item.link">
          {{ item.title }}
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
  </div>
</template>


<script>
module.exports = {
  data() {
    return {
      drawer: false,
      items: [
        { title: "Home", link: "/" },
        { title: "Token", link: "/token" },
      ],
    };
  },
};
</script>