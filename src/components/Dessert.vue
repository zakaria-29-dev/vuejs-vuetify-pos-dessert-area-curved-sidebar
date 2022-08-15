<template>
      <v-item-group mandatory class="mt-n4">
        <v-container>
          <v-row justify="center" class="space">
            <v-col
              cols="12"
              xs="12"
              sm="4"
              md="2"
              v-for="(cetegory, i) in categories"
              :key="i"
            >
              <v-item v-slot="{ active, toggle }">
                <v-card
                  :color="active ? '#FFCB5E' : 'white'"
                  :class="active ? 'borderme' : 'borderout'"
                  class="d-flex align-center rounded-lg mx-2"
                  dark
                  height="120"
                  @click="toggle"
                  flat
                >
                  <v-row>
                    <v-col cols="12" sm="12">
                      <v-list-item three-line class="text-center">
                        <v-list-item-content>
                          <div align="center" justify="center">
                            <v-img
                              :src="cetegory.img"
                              max-height="80"
                              max-width="80"
                              contain
                            ></v-img>
                          </div>
                        </v-list-item-content>
                      </v-list-item>
                    </v-col>
                  </v-row>
                </v-card>
              </v-item>
            </v-col>
          </v-row>
        </v-container>
      </v-item-group>
</template>

<script>
export default {
data: () => ({
    categories: [
      { img: "f1.png" },
      { img: "f2.png" },
      { img: "f3.png" },
      { img: "f4.png" },
      { img: "f5.png" },
    ],
})
}
</script>

<style>

</style>