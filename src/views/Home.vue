<template>
  <v-app
    id="inspire"
    :style="{ background: $vuetify.theme.themes.dark.background }"
  >
    <SideBar />
    <RightSideBar />
    <v-container>
     <Navbar />
      <dessert />
      <v-toolbar flat color="transparent" class="mt-n4">
        <v-toolbar-title class="ml-4">
          <strong>Day</strong><span class="grey--text ml-2">Menu</span>
        </v-toolbar-title>
      </v-toolbar>
        <Menu />


      <v-toolbar flat color="transparent" class="mt-n4">
        <v-toolbar-title class="ml-4">
          <strong>Ingredients</strong><span class="grey--text ml-2">Food</span>
        </v-toolbar-title>
      </v-toolbar>
      <Food />
     <Comment />
    </v-container>
  </v-app>
</template>

<script>
// @ is an alias to /src
import SideBar from "@/components/SideBar.vue";
import RightSideBar from "@/components/RightSideBar.vue";
import Navbar from '../components/Navbar.vue';
import Dessert from '../components/Dessert.vue';
import Menu from '../components/Menu.vue';
import Food from '../components/Food.vue';
import Comment from '../components/Comment.vue';

export default {
  name: "Home",
  data: () => ({
    
   
  }),
  components: {
    SideBar,
    RightSideBar,
    Navbar,
    Dessert,
    Menu,
    Food,
    Comment
  },
};
</script>
