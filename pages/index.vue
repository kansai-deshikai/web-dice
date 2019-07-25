<template>
  <div class="container">
    <div class="header">
      <h1 class="title">
        Webサイコロ
      </h1>
    </div>
    <div class="content">
      <div class="dice-input">
        <div class="form">
          <div class="input-field">
            <input type="number" class="dice-num" v-model="diceDim" /><span class="left-padding">面サイコロ</span>
          </div>
          <div>
            <button v-on:click="roll">{{diceDim}}面サイコロを振る</button>
          </div>
        </div>
      </div>
      <div class="dice-output">{{result}}</div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      diceDim: 6,
      result: null,
    };
  },
  methods:{
    roll() {
      this.result = Math.floor( Math.random() * this.diceDim );
    }
  }
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
  display: flex;
  align-items: center;
  justify-content: center;
}

.dice-input .input-field {
  margin: 1rem;
}

.dice-num {
  width: 100px;
  height: 60px;
  font-size: 50px;
  text-align: right;
}

.left-padding {
  padding-left: 1rem;
}

.dice-input button {
  width: 200px;
  height: 70px;
  font-size: 18px;
}

.dice-output {
  border: 1px solid gray;
  font-size: 200px;
}
</style>
