<template>
  <v-container fluid>
    <v-row>
      <v-col cols="6">
        <v-img src="logo.svg" contain max-height="300" alt="gambar"></v-img>
        <!-- <v-icon color="#A7121D" size="300px" style="align:middle;">fas fa-atom</v-icon> -->
      </v-col>
      <v-col cols="6">
        <h4 class="red--text text--darken-4 top">Hello, Saya </h4>
        <h1 class="white--text">Ardiana Iqbal</h1>
        <h3 class="white--text">Front End Enthusiast</h3>
        <p class="grey--text">
          Selamar datang di laman web saya!
        </p>
        <v-btn tile color="#A7121D" dark @click="scroll('contact')"> Hubungi Saya </v-btn>
      </v-col>
    </v-row>
    <AboutMe />
    <br>
    <MyProject />
    <br>
    <ContactMe />
  </v-container>
</template>

<script>
import AboutMe from './AboutMe.vue';
import ContactMe from './ContactMe.vue';
import MyProject from './MyProject.vue'
export default {
  components: {
    AboutMe,
    ContactMe,
    MyProject,
  },
  methods: {
    scroll(refName) {
      const element = document.getElementById(refName);
      element.scrollIntoView({ behavior: "smooth" });
    },
  },
};
</script>
<style>
@import "../style.css";
</style>
<!-- <style>
.top {
  margin-top: 180px;
}

.topInverse {
  margin-top: -250px;
}

.topTolbar {
  margin-top: 100px;
  text-align: center;
}

.first {
  width: 100%;
  height: 610px;
  background: linear-gradient(to right,
      #181818,
      #181818 50%,
      #111111 50%,
      #111111 50%);
  text-align: center;
  padding: 2rem 2rem;
}

.second {
  width: 100%;
  height: 400px;
  background: #181818;
  text-align: center;
  padding: 2rem 2rem;
}

.secondchild1 {
  display: inline-block;
  background-color: #1e1e1e;
  padding: 2rem 1rem;
  vertical-align: middle;
  text-align: left;
  margin-top: 250px;
}

.child {
  display: inline-block;
  padding: 2rem 1rem;
  vertical-align: middle;
  text-align: left;
  margin-right: 8px;
}

.bgColor1 {
  background-color: #1e1e1e;
}

.bgColor2 {
  background-color: #ce1d2a;
}

.child1 {
  display: inline-block;
  padding: 2rem 1rem;
  vertical-align: middle;
  margin-right: 5px;
  width: 240px;
}

.child2 {
  display: inline-block;
  width: 245px;
  vertical-align: middle;
}

.mRight {
  margin-right: 8px;
}

.mButton {
  margin-bottom: 8px;
}

.padding {
  padding: 8px 0;
}

.col-12.padd {
  padding: 12px 0 !important;
}

.col-12.childcol {
  padding: 0 !important;
}

h1.number {
  font-size: 50px;
  font-weight: bold;
}
</style> -->
