<template>
  <div id="text-input-container">
    <input id="text-input" type="text">
  </div>
</template>

<script>
export default {
  name: "TextInput"
};
</script>

<style>
#text-input {
  display: flex;
  background-color: #3f4042;
  display: flex;
  align-self: center;
  flex: 1;
  border-width: 0;
  height: 100%;
}

#text-input-container {
  width: 100%;
  display: flex;
  flex: 1;
  align-items: center;
}
</style>

