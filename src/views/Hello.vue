<template>
  <div class="hello">
    <h1>This is a hello page, to test some components!</h1>
    <Button text="Click Me!"></Button>
  </div>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import Button from '@/components/Button.vue'; // @ is an alias to /src

@Options({
  components: {
    Button,
  },
})
export default class Hello extends Vue {}
</script>