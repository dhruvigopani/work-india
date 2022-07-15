<template>
  <v-container>
    <v-row class="text-center">
      <v-col cols="4">
        <h1>Applied</h1>
        <v-container 
            v-for="item in list"
            :key="item.id"
          >
          <v-card            
            v-if="item.status == 'Applied'"
            class="mx-auto my-12"
            max-width="374"
          >
            <v-card-title>
              {{ item.name }}
            </v-card-title>

            <v-card-text>
              <v-row align="center" class="mx-0">
                <img src="https://via.placeholder.com/18x18" width="14px" />

                <div class="ms-4">
                  {{ item.last_updated_at }}
                </div>
              </v-row>

              <v-row align="center" class="mx-0">
                <img src="https://via.placeholder.com/18x18" width="14px" />

                <div class="ms-4">
                  {{ item.location }}
                </div>
              </v-row>

              <v-row align="center" class="mx-0">
                <img src="https://via.placeholder.com/18x18" width="14px" />

                <div class="ms-4">
                  {{ item.gender }}
                </div>
              </v-row>
            </v-card-text>
          </v-card>
        </v-container>
      </v-col>

      <v-col cols="4">
        <h1>Accepted</h1>
        <v-container 
            v-for="item in list"
            :key="item.id"
          >
          <v-card            
            v-if="item.status == 'Accepted'"
            class="mx-auto my-12"
            max-width="374"
          >
            <v-card-title>
              {{ item.name }}
            </v-card-title>

            <v-card-text>
              <v-row align="center" class="mx-0">
                <img src="https://via.placeholder.com/18x18" width="14px" />

                <div class="ms-4">
                  {{ item.last_updated_at }}
                </div>
              </v-row>

              <v-row align="center" class="mx-0">
                <img src="https://via.placeholder.com/18x18" width="14px" />

                <div class="ms-4">
                  {{ item.location }}
                </div>
              </v-row>

              <v-row align="center" class="mx-0">
                <img src="https://via.placeholder.com/18x18" width="14px" />

                <div class="ms-4">
                  {{ item.gender }}
                </div>
              </v-row>
            </v-card-text>
          </v-card>
        </v-container>
      </v-col>

      <v-col cols="4">
        <h1>Rejected</h1>
        <v-container 
            v-for="item in list"
            :key="item.id"
          >
          <v-card            
            v-if="item.status == 'Rejected'"
            class="mx-auto my-12"
            max-width="374"
          >
            <v-card-title>
              {{ item.name }}
            </v-card-title>

            <v-card-text>
              <v-row align="center" class="mx-0">
                <img src="https://via.placeholder.com/18x18" width="14px" />

                <div class="ms-4">
                  {{ item.last_updated_at }}
                </div>
              </v-row>

              <v-row align="center" class="mx-0">
                <img src="https://via.placeholder.com/18x18" width="14px" />

                <div class="ms-4">
                  {{ item.location }}
                </div>
              </v-row>

              <v-row align="center" class="mx-0">
                <img src="https://via.placeholder.com/18x18" width="14px" />

                <div class="ms-4">
                  {{ item.gender }}
                </div>
              </v-row>
            </v-card-text>
          </v-card>
        </v-container>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import Vue from "vue";
import VueAxios from "vue-axios";
import axios from "axios";
Vue.use(VueAxios, axios);
export default {
  name: "HelloWorld",
  data() {
    return {
      list: undefined,
    };
  },
  mounted() {
    Vue.axios
      .get("https://run.mocky.io/v3/ae511409-8c0e-40ed-9336-aebcb602823d")
      .then((response) => {
        this.list = response.data.data;       
        console.warn(response.data.data);
      });
  },
};
</script>

<style>
.container{
  padding: 0px;
}
</style>