<template>
  <link href="./dist/output.css" rel="stylesheet">
 <signIn/>
 <secondSignIn/>
</template>

<script>
import signIn from './components/signIn.vue'
import secondSignIn from './components/secondSignIn.vue'
export default {
  name: 'App',
  components: {
    signIn,
    secondSignIn,
    
  }
}
</script>



