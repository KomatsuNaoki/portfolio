<template>
  <div class="content">
    <v-container>
      <v-row class="text-center">

        <v-col class="mb-4">
          <h2 class="display-2 font-weight-bold mb-3">
            KOMATSUBARA TATSUYA
          </h2>

          <p class="subheading font-weight-regular">
            Researchs / Images
          </p>
        </v-col>

        <v-col
          class="mb-5"
          cols="12"
        >

          <v-row justify="center">
            <v-btn @click="goProfile()">Profile</v-btn>
          </v-row>
        </v-col>

        <v-col
          class="mb-5"
          cols="12"
        >

          <v-row justify="center">
            <v-btn @click="goWorks()">Works</v-btn>
          </v-row>
        </v-col>

        <v-col
          class="mb-5"
          cols="12"
        >

          <v-row justify="center">
            <v-btn @click="goContact()">Contact</v-btn>
          </v-row>
        </v-col>
      </v-row>
    </v-container>
  </div>

</template>

<script>
export default {
  name: 'HelloWorld',
  methods: {
    goProfile () {
      console.log('hello')
      this.$router.push('/profile')
    },
    goWorks () {
      console.log('hello')
      this.$router.push('/works')
    },
    goContact () {
      console.log('hello')
      this.$router.push('/contact')
    }
  }
}
</script>
