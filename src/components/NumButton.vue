<template>
  <div id="num-button-container">
    <button id="button">
      <p id="button-text">{{value}}</p>
    </button>
  </div>
</template>
   
<script>
export default {
  name: "NumButton",
  props: {
    value: {
      type: Number,
      required: true
    }
  }
};
</script>

<style>
#num-button-container {
  display: flex;
  flex: 1;
}

#button {
  display: flex;
  flex: 1;
  align-items: center;
  justify-content: center;
  background-color: #000;
  border-width: 0;
}

#button-text {
  font-size: 3em;
  color: orange;
}
</style>
