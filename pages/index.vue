<template>
  <main>
    <div class="background"><app-masthead /></div>
    <div class="headings">
      <h1>
        Hello tacoface!<br/>
        I love tacos.
      </h1>
      <p>Please eat tacos.</p>
    </div>
    <div class="links"><p>Go follow Phil Hawkesworth.</p></div>
    <div class="nextpage">Projects</div>
  </main>
</template>

<script>
  import AppMasthead from '@/components/AppMasthead.vue'
  
  export default {
    components: {
      AppMasthead
    },
  }
</script>

<style lang="scss" scoped>
  main {
    width: 100vw;
    height: calc(100vh - 100px);
  display: grid;
  grid-template-columns: repeat(2, 100px) repeat(3, 1fr);
  grid-template-rows: repeat(5, 1fr);
  grid-column-gap: 0px;
  grid-row-gap: 0px;
  }

  .background { grid-area: 1 / 3 / 5 / 6; }
  .headings { grid-area: 2 / 2 / 3 / 6; }
  .links { 
    grid-area: 5 / 1 / 6 / 5; 
    padding: 30px;

  }
  .nextpage { 
    grid-area: 4 / 5 / 6 / 6; 
    background: #eee;
    color: black;
    padding: 30px;
  }

</style>