<template>
  <button class="slot-style" :style="slotStyle()"><slot /></button>
</template>

<script>
export default {
  props: {
    bgColor: {
      type: String,
    },
    color: {
      type: String,
    },
    width: {
      type: String,
    },
    height: {
      type: String,
    },
  },
  methods: {
    slotStyle() {
      return `background-color:${this.bgColor}; color:${this.color}; width:${this.width}; height:${this.height}; margin-left:15px;`;
    },
  },
};
</script>

<style lang="scss" scoped>
.slot-style {
  padding: 15px;
  width: 300px;
  height: 300px;
  box-shadow: 0 3px 5px -1px rgba(0, 0, 0, 0.2), 0 6px 10px 0 rgba(0, 0, 0, 0.14),
    0 1px 18px 0 rgba(0, 0, 0, 0.12);
}
</style>
