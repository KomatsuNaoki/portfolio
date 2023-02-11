<template>
    <div class="win">
        <div class="content">
            <v-row
            justify="center"
            v-for="(mPU, index) in title"
            :key="index"
            >
                <about-box :title="title[index]" :text="text[index]"></about-box>
            </v-row>
        </div>
        <back-home></back-home>
    </div>
</template>

<script>
import BackHome from '../components/BackHome'
import AboutBox from '../components/AboutBox'
export default {
  name: 'ProfileView',
  components: {
    BackHome,
    AboutBox
  },
  data () {
    return {
      title: ['氏名', '所属', '経歴'],
      text: ['小松原達哉', 'FMS', 'FMS']
    }
  }
}
</script>

<style>

.win {
    height: 100%;
}

.content {
    width:100%;
}

</style>
