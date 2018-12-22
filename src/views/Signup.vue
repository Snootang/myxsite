<template>
  <div class="signup">
    <h1>Enter your account</h1>
    <mInput mkey="Name:" v-model="username"></mInput>
    <mInput mkey="Password:" v-model="password" type="password"></mInput>
    <mButton functext="SignUp" @btnclick="signup"></mButton>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';
import { State } from 'vuex-class'
import mInput from '@/components/utils/Input.vue'; // @ is an alias to /src
import mButton from '@/components/utils/Button.vue'; // @ is an alias to /src

@Component({
  components: {
    mInput,
    mButton,
  },
})
export default class Signup extends Vue {
  username: String = ''
  password: String = ''

  signup() {
    console.log(1)
  }
}
</script>
