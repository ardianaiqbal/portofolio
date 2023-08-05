<template>
  <v-row>

    <div class="first" style="background-color: #A7121D!important;">
      <div class="child" id="contact">
        <v-row>
          <br>
          <v-sheet width="600">
            <h1 class="white--text bgColor2" style="text-align:center ;border-color: #A7121D;border-style: solid;">Hubungi
              Saya</h1>
            <v-form fast-fail @submit.prevent class="bgColor1 white--text" ref="form">
              <p>Nama Lengkap</p>
              <v-text-field v-model="fullName" label="Nama Lengkap" :rules="firstNameRules" style="border-color: #A7121D;"
                color="#A7121D" class="custom-label-color"></v-text-field>
              <p>E-mail</p>
              <v-text-field v-model="email" label="E-mail" placeholder="example@example.com"
                style="border-color: #A7121D;" color="#A7121D" class="custom-label-color"></v-text-field>
              <p>Pesan</p>
              <v-textarea v-model="message" label="Pesan" style="border-color: #A7121D;" color="#A7121D"
                class="custom-label-color" bg-color="#A7121D"></v-textarea>
              <v-btn type="submit" block tile color="#A7121D" @click="reset">Submit</v-btn>
            </v-form>
          </v-sheet>



          <!-- <v-col cols="7">
              <h1 class="white--text">
                Let's work together on<br />your next project
              </h1>
              <p class="grey--text">
                Lorem ipsum dolor sit amet consectetur adipisicing elit.
                Eius nesciunt ducimus natus <br />
              </p>
            </v-col> -->
          <!-- <v-col cols="5">
              <v-btn tile color="#A7121D" dark class="mt-16">
                Contact
              </v-btn>
            </v-col> -->
        </v-row>
      </div>
    </div>
    <!-- <v-toolbar class="topTolbar" color="#111111" dark flat>
        <div style="
                position: absolute;
                margin-left: auto;
                margin-right: auto;
                left: 0;
                right: 0;
                text-align: center;
              ">
          <v-btn text>Home</v-btn>
          <v-btn text>Project</v-btn>
          <v-btn text>about</v-btn>
          <v-btn text> contact</v-btn>
        </div>
      </v-toolbar> -->

  </v-row>
</template>

<script>
export default {
  data: () => ({
    firstName: '',
    firstNameRules: [
      value => {
        if (value?.length > 3) return true

        return 'First name must be at least 3 characters.'
      },
    ],
    lastName: '123',
    lastNameRules: [
      value => {
        if (/[^0-9]/.test(value)) return true

        return 'Last name can not contain digits.'
      },
    ],
  }),
  methods: {
    reset() {
      this.$refs.form.reset()
    },
  }

};
</script>

<style scoped></style>