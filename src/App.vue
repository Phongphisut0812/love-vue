<template>
  <div id="app">
    <div>
      <carousel />
    </div>
    <div class="row mt-5">
      <div class="col-md-6">
        <div>
          <img class="img-circle" alt="Vue logo" src="./assets/h1.jpg" width="auto" height="350px" />
          <Counter @cc="sum" />
        </div>
      </div>
      <div class="col-md-3 a">
        <h1>Total = {{total}}</h1>
      </div>
    </div>
    <div class="row mt-4">
      <div class="col-md-6">
        <div>
          <img class="img-circle" alt="Vue logo" src="./assets/h2.jpg" width="auto" height="350px" />
          <Counter @v="sumb" />
        </div>
      </div>
      <div class="col-md-3 a">
        <h1>Total = {{totl}}</h1>
      </div>
    </div>
    <div class="row mt-4">
      <div class="col-md-6">
        <div>
          <img class="img-circle" alt="Vue logo" src="./assets/h3.jpg" width="auto" height="350px" />
          <Counter @v="num" />
        </div>
      </div>
      <div class="col-md-3 a">
        <h1>Total = {{tota}}</h1>
      </div>
    </div>
    <footer class="footer mt-5">
      <strong>&copy; 2014-2019 Phongphisut</strong>
    </footer>
  </div>
</template>
<script>
import Counter from "./components/Counter";
import carousel from "./components/carousel";
export default {
  name: "App",
  components: {
    Counter,
    carousel,
  },
  data: function () {
    return {
      total: 0,
      totl: 0,
      tota: 0,
    };
  },
  methods: {
    sum(counterValue) {
      this.total += counterValue;
    },
    sumb(countValue) {
      this.totl += countValue;
    },
    num(conter) {
      this.tota += conter;
    },
  },
};
</script>
<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
.a {
  margin: auto;
  margin-left: auto;
  margin-right: auto;
}
.img-circle {
  border-radius: 9%;
}
.footer {
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
