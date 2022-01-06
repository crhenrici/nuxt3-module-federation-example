<template>
  <div>
    <h1>This message in microfrontend-second comes from app {{ msg }}</h1>
    <h1>Config foo: {{ config.foo }}</h1>
  </div>
</template>

<script lang="ts">
import { defineComponent } from '@vue/runtime-core'

export default defineComponent({
  name: 'TestVue',
  props: {
    msg: String,
    config: Object
  }
})
</script>
