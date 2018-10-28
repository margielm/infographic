<template>
  <div class="service">
    <div class="service__header">
      <span class="service__name">Voice MOC</span>
      <span class="service__volume">33 Milion Minutes</span>
    </div>
    <div class="service__countries">
      <top-countries></top-countries>
    </div>
  </div>
</template>

<script>
import TopCountries from './TopCountries';
  export default {
    components: {
      TopCountries
    }
  };
</script>

<style lang="scss" scoped>
  .service {
    display: flex;
    flex-direction: column;
    height: 100%;
  }
  
  .service__header {
    background-color: #b3b3b3;
    display: flex;
    flex-direction: column;
    padding: 25px 15px 25px 15px;
  }
  
  .service__name {
    font-size: 1.2rem;
    margin-bottom: 10px;
    font-weight: bold;
  }
  
  .service__volume {
    font-size: 1.7rem;
    font-weight: bold;
  }
  
  .service__countries {
    background-color: #f1f1f1;
    flex-grow: 1;
    padding-top: 25px;
    padding-bottom: 25px;
  }
</style>


