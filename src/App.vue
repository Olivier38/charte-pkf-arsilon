<template>
  <main id="app">
    <section class="container">
    <h2>Couleurs Primaires</h2>
    <div class="primary">
      <PrimColor v-for="PrimColor in PrimColors"
      :key="PrimColor.name"
      :PrimColor="PrimColor"
      />
    </div>
    <h2>Couleurs Secondaires</h2>
    <div class="secondary">
      <SecondColor v-for="SecondColor in SecondColors"
      :key="SecondColor.name"
      :SecondColor="SecondColor"
      />
    </div>
    </section>
  </main>
</template>

<script>
import PrimColor from './components/PrimColor';
import SecondColor from './components/SecondColor';

export default {
  name: 'App',
  components: {
    PrimColor,
    SecondColor
  },
  data() {
    return {
      show: false,
      PrimColors: [
        {name: 'bleu', cmjn: 'C100 - M75 - J0 - N6', rvb: 'R0 - V53 - B148', hexa: '#003594', pantone: '661 C'},
        {name: 'noir', cmjn: 'N100', rvb: 'R0 - V0 - B0', hexa: '#000000', pantone: 'PANTONE BLACK'},
        {name: 'gris', cmjn: 'C20 - M14 - J12 - N40', rvb: 'R151 - V153 - B155', hexa: '#97999B', pantone: 'COOL GREY 7'},
      ],
      SecondColors: [
        {name: 'light-blue', cmjn: 'C75 - M0 - J5 - N40', rvb: 'R0 - V142 - B32', hexa: '#00B5E2', pantone: 'Pantone 306'},
        {name: 'mid-blue', cmjn: 'C100 - M0 - J20 - N0', rvb: 'R0 - V142 - B170', hexa: '#008EAA', pantone: 'Pantone 3135'},
        {name: 'light-green', cmjn: 'C65 - M0 - J100 - N0', rvb: 'R120 - V190 - B32', hexa: '#78BE20', pantone: 'Pantone 368'},
        {name: 'dark-green', cmjn: 'C47 - M11 - J99 - N64', rvb: 'R89 - V98 - B29', hexa: '#59621D', pantone: 'Pantone 378'},
        {name: 'yellow', cmjn: 'C0 - M19 - J99 - 64', rvb: 'R255 - V199 - B44', hexa: '#FFC72C', pantone: 'Pantone 123'},
        {name: 'lime', cmjn: 'C18 - M0 - J82 - N0', rvb: 'R210 - V228 - B66', hexa: '#DBE442', pantone: 'Pantone 360'},
        {name: 'orange', cmjn: 'C0 - M65 - J100 - N0', rvb: 'R254 - V80 - B0', hexa: '#FE5000', pantone: 'Pantone 021'},
        {name: 'red', cmjn: 'C0 - M96 - J93 - N2', rvb: 'R210 - V38 - B48', hexa: '#D22630', pantone: 'Pantone 1795'},
        {name: 'pink', cmjn: 'C20 - M89 - J0 - N0', rvb: 'R197 - V41 - B155', hexa: '#C5299B', pantone: 'Pantone 240'},
        {name: 'purple', cmjn: 'C66 - M100 - J8 - N27', rvb: 'R100 - V38 - B103', hexa: '#642667', pantone: 'Pantone 260'}
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

#app {
  height: 100%;
}
.container {
  margin: 0px auto;
  width: 55%;
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  flex-direction: column;
  max-height: 80%;
}

.color {
  width: 175px;
  margin: 1px 1px;
  height: 25vh;
  cursor: pointer;
}

.content {
  color: #FFFFFF;
  font-family: Arial, Helvetica, sans-serif;
  font-size: 12px;
  position: relative;
  margin: 15px;
}

.primary, .secondary {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  align-content: flex-start;
}

.primary {
  margin-bottom: 2vh;
}

.colorName {
  font-size: 14px;
  margin-bottom: 2vh;
  text-transform: uppercase
}

h2 {
  font-family: Arial, Helvetica, sans-serif;
}

.details {
  margin-bottom: 5px;
}

.show {
  height: 30px;
  color: rgb(255, 255, 255);
  text-transform: uppercase;
  margin: 50px 0px;
  width: 100%;
  flex: row;
}
.text-show {
  position: relative;
  height: 30px;
  top: -5px;

}

.gg-chevron-down-o {
    box-sizing: border-box;
    position: relative;
    display: inline-block;
    transform: scale(var(--ggs,1));
    width: 22px;
    height: 22px;
    border: 2px solid;
    border-radius: 100px;
    margin: 0px 5px 0px 0px;
}
.gg-chevron-down-o::after {
    content: "";
    display: block;
    box-sizing: border-box;
    position: absolute;
    width: 6px;
    height: 6px;
    border-bottom: 2px solid;
    border-right: 2px solid;
    transform: rotate(45deg);
    left: 6px;
    top: 5px
}
</style>
