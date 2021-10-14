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
  <!-- <div id="app">
    <AppLayout>
      <template v-slot:header>
        I was made with Vue slots!
      </template>
      <AppButton><img src="home.svg" /> Home</AppButton>
      <template v-slot:footer>
        By Robert Baumgartner
      </template>
    </AppLayout>
  </div> -->

  <!-- 
  Antwort auf 2: spielt keine Rolle, da man bei dem slot angibt, 
  ob es ein Footer oder ein Header ist 
  -->

<!-- Aufgabe 3 -->
  <div id="app">
    <DataTable :items="desserts" :headers="headers">
      <template v-slot:header>
        <h2>Don't Watch What You Eat!</h2> <br>
      </template>
      <template v-slot:footer> Created 2021 by Haroon Younas </template>
      <template v-slot:body_content>
        <tr class="last-row">
          <td><b>Total</b></td>
          <td><b>{{ totalCalories }}</b></td>
          <td><b>{{ totalFat }}</b></td>
          <td><b>{{ totalCarbs }}</b></td>
          <td><b>{{ totalProtein }}</b></td>
          <td></td>
        </tr>
      </template>
    </DataTable>
  </div>
</template>

<script>
// import AppButton from '@/components/AppButton.vue';
// import Sheet from '@/components/Sheet.vue';
// import AppLayout from '@/components/AppLayout.vue';
import DataTable from '@/components/DataTable.vue';
export default {
  name: 'App',

  components: {
    // AppButton,
    // Sheet,
    // AppLayout,
    DataTable,
  },

  data() {
    return {
      headers: [
        {
          text: 'Dessert (100g serving)',
          value: 'dessert',
        },
        { text: 'Calories', value: 'calories' },
        { text: 'Fat (g)', value: 'fat' },
        { text: 'Carbs (g)', value: 'carbs' },
        { text: 'Protein (g)', value: 'protein' },
        { text: 'Iron (%)', value: 'iron' },
      ],
      desserts: [
        {
          dessert: 'Frozen Yogurt',
          calories: 159,
          fat: 6.0,
          carbs: 24,
          protein: 4.0,
          iron: '1%',
        },
        {
          dessert: 'Ice cream sandwich',
          calories: 237,
          fat: 9.0,
          carbs: 37,
          protein: 4.3,
          iron: '1%',
        },
        {
          dessert: 'Eclair',
          calories: 262,
          fat: 16.0,
          carbs: 23,
          protein: 6.0,
          iron: '7%',
        },
        {
          dessert: 'Cupcake',
          calories: 305,
          fat: 3.7,
          carbs: 67,
          protein: 4.3,
          iron: '8%',
        },
        {
          dessert: 'Gingerbread',
          calories: 356,
          fat: 16.0,
          carbs: 49,
          protein: 3.9,
          iron: '16%',
        },
      ],
    };
  },
  computed: {
    totalCalories() {
      return this.desserts.map((el) => el.calories).reduce((p, c) => p + c);
    },
    totalFat() {
      return this.desserts.map((el) => el.fat).reduce((p, c) => p + c);
    },
    totalCarbs() {
      return this.desserts.map((el) => el.carbs).reduce((p, c) => p + c);
    },
    totalProtein() {
      return this.desserts.map((el) => el.protein).reduce((p, c) => p + c);
    },
  },
};
</script>

<style scoped>
#app {
  text-align: center;
}
</style>
