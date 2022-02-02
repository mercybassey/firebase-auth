<template>
  <div>
    <form  @submit.prevent="onSubmit">
      <h1>Log In</h1>
      <label for="text">Name</label>
      <input type="text" name="name" placeholder="Name" required>

      <label for="email">Email</label>
      <input type="email" name="email" placeholder="Email" required>

      <label for="password">Password</label>
      <input type="password" name="password" placeholder="Password" required>

      <button class="email"><i class="far fa-envelope"></i>Log In </button>
      <button class="google"><i class="fab fa-google"></i>Google</button>
      <button class="apple"><i class="fab fa-apple"></i>Apple </button>
      <button class="facebook"><i class="fab fa-facebook-f"></i>Facebook </button>
      <button class="github"><i class="fab fa-github"></i>Github </button>
       <button class="twitter"><i class="fab fa-twitter"></i>Twitter</button>
    </form>
  </div>
</template>

<script>
import {ref} from 'vue';
export default {
  
  name: 'Register',

  setup() {
    const name = ref("")
    const email = ref("")
    const password = ref("")

    const onSubmit = () => {
      console.log('form submitted')
    }

    return{name, email, password, onSubmit}
  },
}
</script>