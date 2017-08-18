<template>
  <div id="app">
    <div class="ui left vertical inverted labeled icon sidebar menu">
    <a class="item">
        <i class="home icon"></i>
        Home
    </a>
    <a class="item">
        <i class="block layout icon"></i>
        Topics
    </a>
    <a class="item">
        <i class="smile icon"></i>
        Friends
    </a>
    <a class="item">
        <i class="calendar icon"></i>
        History
    </a>
    <a class="item">
        <i class="mail icon"></i>
        Messages
    </a>
    <a class="item">
        <i class="chat icon"></i>
        Discussions
    </a>
    <a class="item">
        <i class="trophy icon"></i>
        Achievements
    </a>
    <a class="item">
        <i class="shop icon"></i>
        Store
    </a>
    <a class="item">
        <i class="settings icon"></i>
        Settings
    </a>
  </div>
  <div class="pusher">
    <!-- Site content !-->
    <img class="sidebar-opener" src="./assets/logo.png">
    <router-view></router-view>

  </div>

  </div>
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      msg: 'This is not the message you were looking for!'
    }
  },
  mounted: function () {
    console.log("MOUNTED");
    this.initializeSemantic();
    this.setupLogoSidebarOpener();
  },
  ready: function () {
    console.log("READY");
    this.initializeSemantic();
    this.setupLogoSidebarOpener();
  },
  methods: {
    initializeSemantic: function () {
      console.log($(this.$el));
      // Update elements to match what is needed by Semantic.js
      $('#app .ui.sidebar').sidebar({context:$('#app')})
      .sidebar('setting', 'transition', 'overlay')
      .sidebar('toggle');
    },
    setupLogoSidebarOpener: function () {
      var swipeMenu = $('#app .ui.sidebar');
      $('.sidebar-opener').click(function () {
        swipeMenu.sidebar('toggle');
      })

    }
}
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
