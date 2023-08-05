<template>
  <v-app-bar app color="#111111" dark flat class="px-8">

    <v-btn text @click="scroll('home')">Beranda</v-btn>
    <v-btn text @click="scroll('about')">Tentang Saya</v-btn>
    <v-btn text @click="scroll('project')">Project</v-btn>
    <v-btn text @click="scroll('contact')"> Hubungi Saya</v-btn>
    <v-spacer></v-spacer>
    <v-btn icon @click="scroll('home')">
      <v-icon color="#A7121D" size="50px">fas fa-atom</v-icon>
    </v-btn>
  </v-app-bar>
</template>

<script>
export default {
  methods: {
    scroll(refName) {
      const element = document.getElementById(refName);
      element.scrollIntoView({ behavior: "smooth" });
    },
  },
};
</script>

<style></style>