<template>
  <div>
    <button v-on:click="loginWithGoogle()">Login With Google</button>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'
import firebase from 'firebase/app'

@Component({
  components: {}
})
export default class Login extends Vue {
  loginWithGoogle (): void {
    const provider = new firebase.auth.GoogleAuthProvider()
    firebase.auth().signInWithPopup(provider).then((result) => {
      console.log(result)
    }).catch((error) => {
      console.error(error)
    })
  }
}
</script>

<style>

</style>
