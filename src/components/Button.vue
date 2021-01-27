<template>
  <div class="button" v-on:click="count++">
     <h1>{{ text }}</h1>
     You clicked me {{ count }} times.
  </div>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';

@Options({
    props: {
        text: String,
    },
    data: function () {
        return {
            count: 0
        }
    }
})
export default class Button extends Vue {
    public hello() {
        console.log('hello');
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
    div {
        user-select: none;
        cursor: pointer;
        border: 0.125rem solid;
        display: inline-flex;
        flex-direction: row;
        justify-content: center;
        align-items: center;
        box-shadow: rgba(0, 0, 0, 0.12) 0px 4px 8px 0px, rgba(0, 0, 0, 0.08) 0px 2px 4px 0px;
        box-sizing: border-box;
        position: relative;
        width: auto;
        min-height: 2.5rem;
        min-width: 5rem;
        text-align: center;
        overflow: hidden;
        border-radius: 0.25rem;
        padding: 0.5rem 1rem;
    }
    div h1 {
        padding: 0;
        margin: 0;
    }
</style>
