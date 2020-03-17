<template>
  <div>
    <canvas id="myCanvas" width="1000" height="800"></canvas>
  </div>
</template>

<script>
export default {
  mounted() {
    // 获取元素
    var canvas = document.getElementById("myCanvas");
    for (var i = 30; i < 600; i += 30) {
      for (var k = 30; k < 800; k += 30)
        if (Math.random() > 0.75) {
          var box = canvas.getContext("2d");
          box.fillStyle = "skyblue";
          box.fillRect(k, i, 20, 20);
        } else if (Math.random() > 0.5 && Math.random() < 0.75) {
          var box1 = canvas.getContext("2d");
          box1.fillStyle = "yellow";
          box1.fillRect(k, i, 20, 20);
        } else if (Math.random() > 0.25 && Math.random() < 0.5) {
          var box2 = canvas.getContext("2d");
          box2.fillStyle = "pink";
          box2.fillRect(k, i, 20, 20);
        } else {
          var box3 = canvas.getContext("2d");
          box3.fillStyle = "purple";
          box3.fillRect(k, i, 20, 20);
        }
    }
  },

};
</script>

<style scoped>
#myCanvas {
  border: 1px solid #ccc;
}
</style>