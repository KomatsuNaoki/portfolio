<template>
  <div class="home">
  <div class="content">
      <!--v-row class="text-center"-->

        <v-col class="mb-1">
          <h2 class="display-2 font-weight-bold mb-1">
            KOMATSUBARA TATSUYA
          </h2>

          <!--p class="subheading font-weight-regular">
            Researchs / Images
          </p-->
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
      <!--/v-row-->
  </div>
</div>

</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      page: 'Home'
    }
  },
  methods: {
    goProfile () {
      this.$router.push('/profile')
    },
    goWorks () {
      this.$router.push('/works')
    },
    goContact () {
      this.$router.push('/contact')
    }
  }
}
</script>
