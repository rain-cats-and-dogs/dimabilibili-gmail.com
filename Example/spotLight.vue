<template>
  <div id="app">
    <h1 data-spotLight="CodingStartUp!">CodingStartUp</h1>
  </div>
</template>
<script>
export default {
}
</script>
<style lang="less" scoped>
html {
  font-size: 15px;
}
body {
  background-color: #eee;
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
  h1 {
    position: relative;
    color: #333;
    font-family: Helvetica, Arial, sans-serif;
    margin: 0;
    padding: 0;
    font-size: 8rem;
    letter-spacing: -0.3rem;
  }
  h1::after {
    content: attr(data-spotLight);
    color: transparent;
    position: absolute;
    top: 0;
    left: 0;
    animation: spotLight 10s infinite;
    background-image: url(https://i0.hdslb.com/bfs/archive/22650682fd25a4a5aa96dd9ef53190c6b8d54912.png);
    background-clip: text;
    -webkit-background-clip: text;
  }
}

@keyframes spotLight {
  0% {
    clip-path: ellipse(100px 100px at 0% 50%);
  }
  50% {
    clip-path: ellipse(100px 100px at 100% 50%);
  }
  100% {
    clip-path: ellipse(100px 100px at 0% 50%);
  }
}
</style>