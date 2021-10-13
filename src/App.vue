<template>
  <div style="display:flex">
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
  </div>
</template>

<script>
// import AppButton from '@/components/AppButton.vue';
import Sheet from '@/components/Sheet.vue';
export default {
  name: 'App',

  components: {
    // AppButton,
    Sheet,
  },

  data: () => ({
    //
  }),
};
</script>
