<template>
  <div class="minput">
    <span class="minput-name">{{mkey}}</span>
    <input class="minput-value" :value="mvalue" :type="type" @input="changed" />
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue, Model, Emit } from 'vue-property-decorator';

@Component
export default class mInput extends Vue {
  @Prop({ default: 'text' }) private type!: string
  @Prop() private mkey!: string

  @Model('input', { type: String }) private mvalue!: String

  @Emit('input')
  changed(ev: any) {
    return ev.target.value
  }
}
</script>

<style scoped lang="scss">
.minput {
  height: 40px;
  line-height: 40px;
  font-size: 20px;
  
  .minput-name {
    display: inline-block;
    width: 100px;
  }

  .minput-value {
    width: 300px;
    font-size: 16px;
    outline: none;
    border: none;
    border-bottom: 1px solid #ccc;

    &:focus {
      border-bottom-color: #3894ff;
    }
  }
}
</style>