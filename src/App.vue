<template>
  <!-- Aufgabe 1 -->
  <!-- <div style="display:flex">
    <Sheet bg-color="#3498db" color="white" width="250" height="300">
      <h3>Memo to myself</h3>
      <p>Always prepare for PLFs in time!</p>
      <img src="info.svg" width="80px" />
    </Sheet>
    <Sheet bg-color="#8e44ad" color="yellow" width="400" height="300">
      <p>INSY, SEW and Webtechnologies are our favorite subjects!</p>
      <span style="font-style: italic">Starkschwitz Fiedler, Jan Schreck</span>
      <p>Wish is was there!</p>
      <span style="font-style: italic">E. Wahn</span>
    </Sheet>
  </div> -->

<!-- Aufgabe 2 -->
  <div id="app">
    <AppLayout>
      <template v-slot:header>
        I was made with Vue slots!
      </template>
      <AppButton><img src="home.svg" /> Home</AppButton>
      <template v-slot:footer>
        By Robert Baumgartner
      </template>
    </AppLayout>
  </div>

  <!-- 
  Antwort auf 2: spielt keine Rolle, da man bei dem slot angibt, 
  ob es ein Footer oder ein Header ist 
  -->
  
</template>

<script>
import AppButton from '@/components/AppButton.vue';
// import Sheet from '@/components/Sheet.vue';
import AppLayout from '@/components/AppLayout.vue';
export default {
  name: 'App',

  components: {
    AppButton,
    // Sheet,
    AppLayout,
  },

  data: () => ({
    //
  }),
};
</script>

<style scoped>
#app {
  text-align: center;
}
</style>
