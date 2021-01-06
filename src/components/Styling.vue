<template>
  <div>
    <header>
      <h1>Vue Dynamic Styling</h1>
    </header>
    <section id="styling">
      <div class="demo"
           :style="{borderColor: box1 ? 'red' : '#ccc'}"
           id="1"
           @click="selectBox(1)"
      >Inline styling</div>
      <div class="demo"
           :class="{demo:true, active: box2}"
           id="2"
           @click="selectBox(2)"
      >Adding classes dynamically</div>
      <div class="demo"
           :class="box3Classes"
           id="3"
           @click="selectBox(3)"
      > Classes & Computed Properties</div>
      <div :class="['demo', {active: box4}]"
           id="4"
           @click="selectBox(4)"
      >Adding classes dynamically with Array Syntax</div>
    </section>
  </div>
</template>

<script>
export default {
  name: "Styling",
  data() {
    return {
      box1: false,
      box2: false,
      box3: false,
      box4: false,
    }
  },
  computed: {
    box3Classes() {
      // Here we can have a more complex logic and have the html cleaner.
      return {active: this.box3}
    }
  },
  methods: {
    selectBox(boxId) {
      switch (boxId) {
        case 1:
          this.box1 = !this.box1;
          break;
        case 2:
          this.box2 = !this.box2;
          break
        case 3:
          this.box3 = !this.box3;
          break;
        case 4:
          this.box4 = !this.box4;
          break;
      }
    }
  }
}
</script>

<style scoped>

</style>
