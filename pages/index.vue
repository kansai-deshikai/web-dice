<template>
  <div class="container">
    <div class="header">
      <h1 class="title">
        Webサイコロ
      </h1>
    </div>
    <div class="content">
      <div class="dice-input"></div>
      <div class="dice-output"></div>
    </div>
  </div>
</template>

<script>
export default {
}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  display: flex;
  flex-direction: column;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.content {
  display: flex;
}

.dice-input, .dice-output {
  width: 400px;
  height: 400px;
  border: 1px solid gray;
}
</style>
