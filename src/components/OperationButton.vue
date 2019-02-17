<template>
  <div id="operation-button-container">
    <button v-bind:style="operationButtonStyle">
      <p id="operation-symbol">{{symbol}}</p>
    </button>
  </div>
</template>

<script>
export default {
  name: "OperationButton",
  props: {
    symbol: {
      type: String,
      required: true
    },
    backgroundColor: {
      type: String,
      default: "#6d6d6d"
    }
  },
  data: function() {
    return {
      operationButtonStyle: {
        display: "flex",
        flex: "1",
        alignItems: "center",
        justifyContent: "center",
        backgroundColor: this.backgroundColor
          ? this.backgroundColor
          : "#6d6d6d",
        borderWidth: 0
      }
    };
  }
};
</script>

<style scoped>
#operation-button-container {
  display: flex;
  flex: 1;
}

#operation-symbol {
  font-size: 2em;
}
</style>