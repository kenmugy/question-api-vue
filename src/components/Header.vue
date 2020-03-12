<template>
  <div class="header">
    <h2 id="logo">Logo</h2>
    <h2 id="score">Counter: 1/4</h2>
  </div>
</template>

<script>
export default {
  name: "Header"
};
</script>

<style>
*,
::before,
::after {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
.header {
  display: flex;
  border-bottom: 2px solid coral;
  margin-bottom: 20px;
}

#score {
  margin-left: 10px;
}
</style>