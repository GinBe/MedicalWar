<template>
  <q-header elevated class="header" height-hint="96">
    <q-tabs align="left">
      <q-route-tab to="/page1" label="Intro" />
      <q-route-tab to="/page2" label="Host" />
      <div class="logo_container">
        <div class="logo" onclick="alert(1)"></div>
      </div>
      <!-- <div class="right">
        <a href="">追波</a>
        <a href="">站酷</a>
        <a href="">站酷</a>
      </div> -->
    </q-tabs>
  </q-header>
</template>

<script>
export default {
  name: "Header",
  data() {
    return {};
  },
};
</script>

<style scoped lang="scss">
$height: 80px;
.header {
  background-color: #1d1d1d;
  height: $height;
  .q-tab{
    height: $height;
    // background-color: red;
  }
  .q-tab__content {
    z-index: 2;
    height: $height;
    font-size: 18px;
    line-height: 24px;
    &:hover {
      background-color: red;
    }
  }
  .q-focus-helper {
    background-color: blue；;
  }

  .right {
    z-index: 2;
    position: absolute;
    right: 20px;
  }

  .right a {
    background-color: green;
    height: 40px;
    display: inline-block;
    margin-left: 10px;
  }

  .logo_container {
    z-index: 1;
    width: 100vw;
    height: $height;
    position: absolute;
    text-align: center;
    pointer-events: none;
  }

  .logo {
    pointer-events: auto;
    background-color: green;
    width: 200px;
    height: $height;
    display: inline-block;
    &:hover {
      background-color: blue;
    }
  }

  .q-avatar {
    margin: 0 10px;
  }
}
</style>
