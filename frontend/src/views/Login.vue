<template>
  <div>
    <navbar/>
    <h1>
      Login
    </h1>
    <login/>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'
import Navbar from '@/components/Navbar.vue'
import Login from '@/components/Login.vue'

@Component({
  components: {
    Navbar,
    Login
  }
})
export default class Home extends Vue {}
</script>
