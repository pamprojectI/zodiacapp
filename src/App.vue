<script setup>
import NavMenu from './components/NavMenu.vue'
import Contant from './components/Contant.vue'
import Footer from './components/Footer.vue'
import items from './zodiac.json'
</script>

<template>
  <header>
    <NavMenu /> 
  </header>

  <main>
    <h1>Zodiac App</h1>
    <div className="grid-container">
      <!-- <Contant v-bind="izos[0]"/>
      <Contant v-bind="izos[1]"/>
      <Contant v-bind="izos[2]"/>
      <Contant v-bind="izos[3]"/>
      <Contant v-bind="izos[4]"/> -->
      <Contant v-for="item in items" :key="item.id" v-bind="item" />
    </div>

    <Footer />
  </main>

</template>

<style scoped>
.grid-container {
  display: grid;
  grid-column-gap: 0.5rem;
  grid-row-gap: 0.5rem;
}

@media (min-width: 576px) {
  .grid-container { grid-template-columns: repeat(1, 1fr); }
}

@media (min-width: 992px) {
  .grid-container { grid-template-columns: repeat(3, 1fr); }
}

</style>
