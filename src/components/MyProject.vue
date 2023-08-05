<template>
  <div class="first" id="project">
    <h1 class="white--text secondchild1">Sayangnya masih belum ada proyek bosku :(</h1>
    <h3 class="grey--text">Kalau minat kerjasama japri langsung 👇</h3>
    <v-btn tile color="#A7121D" dark @click="scroll('contact')"> Hubungi Saya </v-btn>
  </div>
</template>

<script>
export default {
  methods: {
    scroll(refName) {
      const element = document.getElementById(refName);
      element.scrollIntoView({ behavior: "smooth" });
    },
  }
};
</script>

<style></style>