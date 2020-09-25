<template>
  <div>
    <p>
      <router-link to="/">home</router-link> |
      <router-link to="/login">login</router-link>
    </p>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'

@Component({
  components: {}
})
export default class Navbar extends Vue {
  get isAuthenticated () {
    return window.location.pathname !== '/login'
  }
}
</script>

<style>

</style>
