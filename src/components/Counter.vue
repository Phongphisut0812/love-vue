<template>
  <div id="example-1 ">
      <button v-on:click="$like" class="button4" > <i class="fas fa-thumbs-up fa-2x "></i> </button>
      <button v-on:click="$love" class="button4"> <i class="fas fa-heart fa-2x "></i> </button>
      <button v-on:click="$haha" class="button4"> <i class="fas fa-laugh-squint fa-2x"></i> </button>
      <button v-on:click="$wow" class="button4"> <i class="fas fa-surprise fa-2x"></i> </button>
      <button v-on:click="$sad" class="button4"> <i class="fas fa-frown fa-2x"></i> </button>
      <button v-on:click="$angry" class="button4"> <i class="fas fa-angry fa-2x"></i> </button>
     
    </div>
</template>

<script>
export default {
 data: function () {
    return {
        like:0,
        love:0,
        haha:0,
        wow:0,
        sad:0,
        angry:0,
      counter: 0,
      
    };
  },
  
   methods: {
    $like: function () {
      this.like = 1;
      this.$emit("cc", this.like);
      this.$emit("v", this.like);
      this.$emit("p", this.like);
    },
    $love: function () {
      this.love = 10;
      this.$emit("cc",this.love);
      this.$emit("v",this.love);
      this.$emit("p", this.love);
    },
    $haha: function () {
      this.haha = 5;
      this.$emit("cc",this.haha);
      this.$emit("v",this.haha);
      this.$emit("p", this.haha);
    },
    $wow: function () {
      this.wow = 20;
      this.$emit("cc",this.wow);
      this.$emit("v",this.wow);
      this.$emit("p", this.wow);
    },
    $sad: function () {
      this.sad =-5;
      this.$emit("cc",this.sad);
      this.$emit("v",this.sad);
      this.$emit("p", this.sad);
    },
    $angry: function () {
      this.angry =-50;
      this.$emit("cc",this.angry);
      this.$emit("v",this.angry);
      this.$emit("p", this.angry);
    },
  },
}
</script>

<style>
.button4 {
  border-radius: 12px;
  background-color: cadetblue;
  
  }

</style>