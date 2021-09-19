<template>
  <main id="app">
    <section class="container">
      <color v-for="color in colors"
      :key="color.name"
      :color="color"
      />
    </section>
  </main>
</template>

<script>
import Color from './components/Color';
export default {
  name: 'App',
  components: {
    Color
  },
  data() {
    return {
      colors: [
        {name: 'bleu', cmjn: 'C100 - M75 - J0 - N6', rvb: 'R0 - V53 - B148', hexa: '#003594', pantone: '661 C'},
        {name: 'noir', cmjn: 'N100', rvb: 'R0 - V0 - B0', hexa: '#000000', pantone: 'PANTONE BLACK'},
        {name: 'gris', cmjn: 'C20 - M14 - J12 - N40', rvb: 'R151 - V153 - B155', hexa: '#97999B', pantone: 'COOL GREY 7'},
        {name: 'light-blue', cmjn: 'C75 - M0 - J5 - N40', rvb: 'R0 - V142 - B32', hexa: '#00B5E2', pantone: 'Pantone 306'},
        {name: 'mid-blue', cmjn: 'C100 - M0 - J20 - N0', rvb: 'R0 - V142 - B170', hexa: '#008EAA', pantone: 'Pantone 3135'},
        {name: 'light-green', cmjn: 'C65 - M0 - J100 - N0', rvb: 'R120 - V190 - B32', hexa: '#78BE20', pantone: 'Pantone 368'},
        {name: 'dark-green', cmjn: 'C47 - M11 - J99 - N64', rvb: 'R89 - V98 - B29', hexa: '#59621D', pantone: 'Pantone 378'},
        {name: 'yellow', cmjn: 'C0 - M19 - J99 - 64', rvb: 'R255 - V199 - B44', hexa: '#59621D', pantone: 'Pantone 123'},
        {name: 'lime', cmjn: 'C18 - M0 - J82 - N0', rvb: 'R210 - V228 - B66', hexa: '#DBE442', pantone: 'Pantone 360'},
        {name: 'orange', cmjn: 'C0 - M65 - J100 - N0', rvb: 'R254 - V80 - B0', hexa: '#FE5000', pantone: 'Pantone 021'},
        {name: 'red', cmjn: 'C0 - M96 - J93 - N2', rvb: 'R210 - V38 - B48', hexa: '#D22630', pantone: 'Pantone 1795'},
        {name: 'pink', cmjn: 'C20 - M89 - J0 - N0', rvb: 'R197 - V41 - B155', hexa: '#C5299B', pantone: 'Pantone 240'},
        {name: 'purple', cmjn: 'C66 - M100 - J8 - N27', rvb: 'R100 - V38 - B103', hexa: '#C5299B', pantone: 'Pantone 260'}
      ]
    }
  }
}
</script>

<style>

.bleu {
  background-color: #003594
}
.noir {
  background-color: #000000;
}
.gris {
  background-color: #97999B;
}
.light-blue {
  background-color: #00B5E2;
}
.mid-blue {
  background-color: #008EAA;
}
.light-green {
  background-color: #78BE20;
}
.dark-green {
  background-color: #59621D;
}
.yellow {
  background-color: #FFC72C;
}
.lime {
  background-color: #DBE442;
}
.orange {
  background-color: #FE5000;
}
.red {
  background-color: #D22630;
}
.pink {
  background-color: #C5299B;
}
.purple {
  background-color: #642667;
}


.container {
  margin: 0 auto;
  width: 50%;
  display: flex;
  justify-content: center;
  flex-wrap: wrap;

}
.color {
  width: 200px;
  height: 33vh;
}
.content {
  color: #FFFFFF;
  margin: 15px;
  font-family: arial;
  font-size: 12px;
  position: relative;
  bottom: 1àpx;

}
</style>
