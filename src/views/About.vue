<template>
  <div class="about">
    <h1>This is an about page</h1>
    <h2>with {{mCount}} clicks.</h2>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';
import { State } from 'vuex-class'

@Component
export default class About extends Vue {
  @State('count') private mCount!: Number;
}
</script>