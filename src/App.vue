<template>
  <div id="app">
    <h1>{{ message }}</h1>
    <BButton @click="show?.({ props: { title: 'Hello', body: 'World' } })">Show</BButton>
    <BToastOrchestrator />
  </div>
</template>


<script>
import { useToastController } from 'bootstrap-vue-next';
const { show } = useToastController()
export default {
  name: 'App',
  data() {
    return {
      message: 'Hello Vue!'
    }
  }
}
</script>
