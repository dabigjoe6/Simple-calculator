<template>
  <div id="app">
    <TextInput/>
    <div id="container">
      <div id="sub-container">
        <div id="operation-container" v-bind:style="top">
          <OperationButton operation="division" symbol="%"/>
          <OperationButton operation="multiplication" symbol="x"/>
        </div>
        <div id="row-container">
          <div class="row">
            <NumButton v-for="number in row1" v-bind:key="number" v-bind:value="number"/>
          </div>
          <div class="row">
            <NumButton v-for="number in row2" v-bind:key="number" v-bind:value="number"/>
          </div>
          <div class="row">
            <NumButton v-for="number in row3" v-bind:key="number" v-bind:value="number"/>
          </div>
        </div>
      </div>
      <div id="operation-container">
        <OperationButton operation="subtraction" symbol="-"/>
        <OperationButton operation="addition" symbol="+"/>
        <div id="assignmentContainer">
          <OperationButton operation="assignment" symbol="=" backgroundColor="orange"/>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import NumButton from "./components/NumButton";
import TextInput from "./components/TextInput";
import OperationButton from "./components/OperationButton";

export default {
  name: "app",
  data: function() {
    return {
      row1: [7, 8, 9],
      row2: [4, 5, 6],
      row3: [1, 2, 3],
      top: {
        flexDirection: "row"
      }
    };
  },
  components: {
    NumButton,
    TextInput,
    OperationButton
  }
};
</script>

<style>
#app {
  display: flex;
  flex-direction: column;
  align-items: center;
  align-self: center;
  width: 30%;
  position: fixed;
  top: 0;
  left: 35%;
  height: 100%;
  background-color: #9e0f0b;
}

#row-container {
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  flex: 3;
}

#container {
  display: flex;
  flex-direction: row;
  width: 100%;
  flex: 3;
}

#sub-container {
  display: flex;
  flex: 3;
  flex-direction: column;
}

#operation-container {
  display: flex;
  flex: 1;
  flex-direction: column;
}

#assignmentContainer {
  display: flex;
  flex: 2;
  background-color: orange;
}

.row {
  display: flex;
  flex-direction: row;
  flex: 1;
  width: 100%;
}
</style>
