<template>
  <div class="mbutton" @click="mclick">{{functext}}</div>
</template>

<script lang="ts">
import { Component, Prop, Vue, Model, Emit } from 'vue-property-decorator';

@Component
export default class mButton extends Vue {
  @Prop() private functext!: string

  @Emit('btnclick')
  mclick() {
  }
}
</script>

<style scoped lang="scss">
.mbutton {
    cursor: pointer;
}
</style>