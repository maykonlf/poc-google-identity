<template>
  <div>
    <navbar/>
    <h1>
      Home
    </h1>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'
import Navbar from '@/components/Navbar.vue'

@Component({
  components: {
    Navbar
  }
})
export default class Home extends Vue {}
</script>
