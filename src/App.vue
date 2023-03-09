<template>
  <v-app class="bg-black">
    <Navbar></Navbar> <!--Navvigator Bar component-->


    <!--Categories Section -->


    <v-container fluid class="mt-16 bg-red-lighten-5 " style="left: 0;">
      <v-card>
        <v-row class="bg-transparent">
          <v-col cols="12" class="bg-transparent d-flex justify-center justify-space-around  mx-2">
            <v-card v-for="(categoryy, i) in categories " :key="i" class="pa-2" flat outline tile>
              <v-img :src="categoryy.path" width="100" cover bg-transparent>

              </v-img>
            </v-card>
          </v-col>
        </v-row>
      </v-card>
    </v-container>


    <!--Options  Section -->


    <v-toolbar color="white " class="px-2 ">
      <v-checkbox v-model="chair" label="Chairs" class="check mt-4"></v-checkbox>
      <v-checkbox v-model="other" label="Others" class="check mt-4"></v-checkbox>
      <v-divider vertical></v-divider>
      <v-btn class="pa-2 ma-4">Leathers color <v-icon right class="ml-2 mb-1">fa-solid fa-caret-right</v-icon></v-btn>
      <v-divider vertical></v-divider>
      <v-btn class="pa-2 ma-4">choose design<v-icon right class="ml-2 mb-1">fa-solid fa-caret-right</v-icon></v-btn>
      <v-divider vertical></v-divider>
      <span class="text-h8 mx-2">Price till</span>
      <v-slider v-model="slider2" label="TRACK COLOR" class="mt-5"></v-slider>
      <span class="text-h8 mx-2">10.000$</span>
    </v-toolbar>
    <v-divider></v-divider>


    <!--Sort Section -->


    <v-toolbar app dark fluid class="bg-white">
      <v-toolbar-title>
        LOUNGUE CHAIR
      </v-toolbar-title>
      <v-spacer>
      </v-spacer>
      <span class="mr-6"><v-btn-toggle v-model="toggle_exclusive">
          <strong class="mt-3 mr-2"> Sort by :</strong>
          <v-btn variant=" text" color=""> Name</v-btn>
          <v-btn variant="text" color=""> Pmopularity </v-btn>
          <v-btn variant="text" color=""> Price</v-btn>
        </v-btn-toggle>
      </span>
    </v-toolbar>


    <!--Product Section -->


    <v-row class=" pa-4 bg-red-lighten-5">
      <v-col cols="12" sm="3" v-for="(chair, i) in chairs" :key="i">
        <v-card height="" align="center" flat outlined tile>
          <v-img :src="chair.image" :class="chair.class" contain width="200" height="200" class="mt-4">
          </v-img>
          <v-card-text class="mt-n1"> <strong> {{ chair.title }} </strong> </v-card-text>
          <v-card-text class="mt-n2"> <strong> {{ chair.price }} </strong> </v-card-text>
        </v-card>
      </v-col>
    </v-row>


    <!--Footer Section -->


    <v-toolbar class="bg-white">
      <v-spacer></v-spacer>
      <v-toolbar-title class="ml-4 mr-2">
        SHOW MORE ...
      </v-toolbar-title>
      <v-divider vertical></v-divider>
      <v-btn class="pa-2 ma-4"><v-icon left class="ml-2 mb-1" align="center">fa-solid fa-caret-left</v-icon></v-btn>
      <h3 align="center" class="mt-1">3</h3>
      <v-btn class="pa-2 ma-4"><v-icon right class="ml-2 mb-1" align="center">fa-solid fa-caret-right</v-icon></v-btn>
    </v-toolbar>


  </v-app>
</template>

<script setup>
import Navbar from './components/Navbar.vue'
import { ref } from 'vue'

const toggle_exclusive = ref(0)

const type = ref(["SLEEPING BEDS", "LOUNGE CHAIRS", "CHAIRS", "OFFICE CHAIRS", "TABLES NIGHTSTANDS", "KITCHEN FURNITURE"]) /* For The future features */
const chair = ref(true)
const other = ref(false)
const slider2 = ref(50)

/* Categories Data */

const categories = ref([
  { path: require('../public/9.png'), title: "SLEEPING BEDS" },
  { path: require('../public/2.png'), title: "LOUNGE CHAIRS" },
  { path: require('../public/1.png'), title: "CHAIRS" },
  { path: require('../public/4.png'), title: "OFFICE CHAIRS" },
  { path: require('../public/8.jpg'), title: "TABLES NIGHTSTANDS" },
  { path: require('../public/6.png'), title: "KITCHEN FURNITURE" },
])

/* Chairs Data*/

const chairs = ref([
  {
    class: "pa-0",
    image: require("../public/c1.jpg"),
    title: "Lounge Chair",
    price: "$ 145.00",
    category: "SLEEPING BEDS",
  },
  {
    class: "pa-0",
    image: require("../public/c2.jpg"),
    title: "Repos",
    price: "$ 145.00",
    category: "SLEEPING BEDS",
  },
  {
    class: "pa-0",
    image: require("../public/c3.png"),
    title: "Modern Lounge",
    price: "$ 145.00",
    category: "LOUNGE CHAIRS",
  },
  {
    class: "pa-0",
    image: require("../public/c4.png"),
    title: "Loby Chair",
    price: "$ 145.00",
    category: "LOUNGE CHAIRS",
  },
  {
    class: "pa-0",
    image: require("../public/c5.png"),
    title: "Modern Lounge",
    price: "$ 145.00",
    category: "CHAIRS",
  },
  {
    class: "pa-0",
    image: require("../public/c6.png"),
    title: "Modern Lounge",
    price: "$ 145.00",
    category: "CHAIRS",
  },
  {
    class: "pa-0",
    image: require("../public/c7.png"),
    title: "Modern Lounge",
    price: "$ 145.00",
    category: "TABLES NIGHTSTANDS",
  },
  {
    class: "pa-0",
    image: require("../public/c8.png"),
    title: "Modern Lounge",
    price: "$ 145.00",
    category: "TABLES NIGHTSTANDS",
  },
  {
    class: "pa-0",
    image: require("../public/c9.png"),
    title: "Modern Lounge",
    price: "$ 145.00",
    category: "TABLES NIGHTSTANDS",
  },
  {
    class: "pa-0",
    image: require("../public/c10.png"),
    title: "Modern Lounge",
    price: "$ 145.00",
    category: "KITCHEN FURNITURE",
  },
  {
    class: "pa-0",
    image: require("../public/c11.png"),
    title: "Modern Lounge",
    price: "$ 145.00",
    category: "KITCHEN FURNITURE",
  },
  {
    class: "pa-0",
    image: require("../public/c12.png"),
    title: "Modern Lounge",
    price: "$ 145.00",
    category: "KITCHEN FURNITURE",
  },
  {
    class: "pa-0",
    image: require("../public/c13.png"),
    title: "Modern Lounge",
    price: "$ 145.00",
    category: "OFFICE CHAIRS",
  },
  {
    class: "pa-0",
    image: require("../public/c14.png"),
    title: "Modern Lounge",
    price: "$ 145.00",
    category: "OFFICE CHAIRS",
  },
  {
    class: "pa-0",
    image: require("../public/c15.png"),
    title: "Modern Lounge",
    price: "$ 145.00",
    category: "CHAIRS",
  },
  {
    class: "pa-0",
    image: require("../public/c16.png"),
    title: "Modern Lounge",
    price: "$ 145.00",
    category: "CHAIRS",
  },
])
</script>