<template>
  <div class="app">
    <JobList :jobs="jobs" />
  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from "vue";
import axios from "axios";
export default defineComponent({
  name: "App",
  components: {},

  setup() {
    //   const state = reactive({
    //     name: "Link",
    //     age: 123 as number,
    //   });
    // },
    // const name = ref("Stella");
    // const age = ref<number | string>(25);
    // return { name, age };

    const info = data() {
      axios.get('https://api.coindesk.com/v1/bpi/currentprice.json')
      .then(response =>(this.info = response))
    }
    ]);

    return { jobs };
  },
});
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  text-decoration-color: blue;
  color: #0a0a0a;
  margin-top: 60px;
}
</style>
