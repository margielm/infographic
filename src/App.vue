<template>
  <div class="template">
    <Header></Header>
    <Title></Title>
    <Description></Description>
    <MainChart></MainChart>
    <Services></Services>
  </div>
</template>

<script>
  import Header from './components/Header';
  import Title from './components/Title';
  import Description from './components/Description';
  import MainChart from './components/MainChart';
  import Services from './components/Services';
  
  export default {
    name: "app",
    components: {
      Header,
      Title,
      Description,
      MainChart,
      Services
    },
  
  };
</script>

<style>
  body {
    font-family: Arial, Helvetica, sans-serif;
    font-size: 16px;
    max-width: 1000px;
    margin: auto;
  }
</style>
