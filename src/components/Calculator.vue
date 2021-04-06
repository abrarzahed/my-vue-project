<template>
  <h3>
    Calculator App <br />
    Vue js <br />
    Css grid
  </h3>
  <div class="calculator">
    <div class="display">{{ current || 0 }}</div>
    <div @click="clear">AC</div>
    <div @click="sign">+/-</div>
    <div @click="percent">%</div>
    <div @click="divide" class="operator">÷</div>
    <div @click="append('7')">7</div>
    <div @click="append('8')">8</div>
    <div @click="append('9')">9</div>
    <div @click="times" class="operator">×</div>
    <div @click="append('4')">4</div>
    <div @click="append('5')">5</div>
    <div @click="append('6')">6</div>
    <div @click="minus" class="operator">-</div>
    <div @click="append('1')">1</div>
    <div @click="append('2')">2</div>
    <div @click="append('3')">3</div>
    <div @click="add" class="operator">+</div>
    <div @click="append('0')" class="zero">0</div>
    <div @click="dot">.</div>
    <div @click="equal" class="operator">=</div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      current: "",
      operator: null,
      privious: null,
      operatorClicked: false,
    };
  },
  methods: {
    clear() {
      this.current = "";
    },
    sign() {
      this.current =
        this.current[0] === "-" ? this.current.slice(1) : `-${this.current}`;
    },
    percent() {
      this.current = `${parseFloat(this.current) / 100}`;
    },
    append(number) {
      if (this.operatorClicked) {
        this.current = "";
        this.operatorClicked = false;
      }
      this.current = `${this.current}${number}`;
    },
    dot() {
      if (this.current.indexOf(".") === -1) {
        this.append(".");
      }
    },
    setPrivious() {
      this.privious = this.current;
      this.operatorClicked = true;
    },
    divide() {
      this.operator = (a, b) => a / b;
      this.setPrivious();
    },
    times() {
      this.operator = (a, b) => a * b;
      this.setPrivious();
    },
    minus() {
      this.operator = (a, b) => a - b;
      this.setPrivious();
    },
    add() {
      this.operator = (a, b) => a + b;
      this.setPrivious();
    },
    equal() {
      this.current = `${this.operator(
        parseFloat(this.current),
        parseFloat(this.privious)
      )}`;
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  text-align: center;
}
.calculator {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-template-rows: minmax(50px, auto);
  font-size: 20px;
  gap: 6px;
  max-width: 550px;
  margin: 30px auto 30px;
}
.calculator div {
  padding: 15px 5px;
  background: #ddd;
  cursor: pointer;
  border-radius: 5px;
  display: grid;
  place-items: center;
}
.calculator div.display {
  grid-column: 1 / -1;
  background: #444;
  color: #fff;
  padding: 30px;
}
.zero {
  grid-column: 1 / span 2;
}
.calculator div.operator {
  background: #ee9e40;
  color: #fff;
}
</style>
