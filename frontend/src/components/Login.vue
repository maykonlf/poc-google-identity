<template>
  <div>
    <v-btn v-on:click="loginWithGoogle()">Login With Google</v-btn>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'
import firebase from 'firebase/app'
import router from '../router/index'

@Component({
  components: {}
})
export default class Login extends Vue {
  loginWithGoogle (): void {
    const provider = new firebase.auth.GoogleAuthProvider()
    firebase.auth().signInWithPopup(provider).then((result) => {
      console.log(result)
      firebase.auth().currentUser.getIdToken(false).then((token) => {
        console.log('token', token)
      })

      router.push('/')
    }).catch((error) => {
      console.error(error)
    })
  }
}
</script>

<style>

</style>
