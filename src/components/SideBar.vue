<template>
  <nav>
    <v-navigation-drawer dark app color="#FFCB5E" width="100">
      <div class="text-center mt-5">
        <v-icon color="#4D2C00" large class="mt-4">fas fa-bars</v-icon>
      </div>
      <v-list flat class="mt-5">
        <v-list-item-group v-model="selectedItem" color="#4D2C00">
          <v-list-item
            v-for="(item, i) in items"
            :key="i"
            active-class="border"
            class="ml-2 my-3"
            :ripple="false"
          >
            <b></b>
            <b></b>
            <v-list-item-icon>
              <v-icon v-text="item.icon" color="#4D2C00"></v-icon>
            </v-list-item-icon>
          </v-list-item>
        </v-list-item-group>
      </v-list>
      <div
        style="
          position: absolute;
          bottom: 20px;
          margin-left: auto;
          margin-right: auto;
          left: 0;
          right: 0;
          text-align: center;
        "
      >
        <v-btn text>
          <v-icon color="#4D2C00">fas fa-sign-out-alt</v-icon>
        </v-btn>
      </div>
    </v-navigation-drawer>
  </nav>
</template>

<script>
export default {
  data: () => ({
    selectedItem: 0,
    drawer: null,
    items: [
      { icon: "fas fa-apple-alt", text: "Discover" },
      { icon: "fas fa-carrot", text: "Stream" },
      { icon: "fas fa-leaf", text: "Community" },
      { icon: "fas fa-lemon", text: "Statistics" },
      { icon: "fas fa-pepper-hot", text: "Statistics" },
      { icon: "fas fa-seedling", text: "Statistics" },
    ],
  }),
};
</script>

<style>
.border {
  background: #f4f5f9;
  border-top-left-radius: 30px;
  border-bottom-left-radius: 30px;
  text-decoration: none;
}
.border b:nth-child(1) {
  position: absolute;
  top: -20px;
  height: 20px;
  width: 83%;
  background: #f4f5f9;

  display: none;
}
.border b:nth-child(1)::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  border-bottom-right-radius: 20px;
  background: #ffcb5e;
}
.border b:nth-child(2) {
  position: absolute;
  bottom: -20px;
  height: 20px;
  width: 83%;
  background: #f4f5f9;
  display: none;
}
.border b:nth-child(2)::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  border-top-right-radius: 20px;
  background: #ffcb5e;
}
.border b:nth-child(1),
.border b:nth-child(2) {
  display: block;
}
</style>
