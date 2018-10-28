<template>
  <div class="services">
    <Service></Service>
    <Service></Service>
    <Service></Service>

    <div class="data__info">
      <span class="info-number">51%</span> <span>of roamers <br/>travel to the<br/>top 10 countries.</span>
    </div>
  
  </div>
</template>

<script>
import Service from './Service';

export default {
  components: {
    Service
  }
};
</script>

<style lang="scss" scoped>
.services {
  display: grid;
  grid-column-gap: 25px;
  grid-template-columns: 1fr 1fr 1fr 2fr;
}



.data__info {
  background-color: #00f4ce;

  font-size: 2rem;
  font-weight: bold;
  padding: 30px;
  display: flex;
  flex-direction: column;
  justify-content: flex-end;
}

.info-number {
  font-size: 4rem;
}
</style>


