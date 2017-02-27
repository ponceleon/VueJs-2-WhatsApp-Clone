<template>
  <div id="app">


    <div id="startup" v-if="loading">
      <svg class="spinner-container" width="65px" height="65px" viewBox="0 0 52 52">
        <circle class="path" cx="26px" cy="26px" r="20px" fill="none" stroke-width="4px" />
      </svg>
    </div>

    <div class="app-wrapper">


      <div id="side" class="pane pane-one">

        <header class="pane-header pane-list-header">
          <div class="pane-list-user">
            <div class="avatar icon-user-default" style="height: 40px; width: 40px; cursor: pointer;">
              <div class="avatar-body"><img src="https://api.adorable.io/avatars/94/abott@adorable.png"
                  draggable="false" class="avatar-image is-loaded"></div>
            </div>
          </div>
          <div class="pane-list-controls">
            <div class="menu menu-horizontal">
              <div class="menu-item">
                <button class="icon" title="Yeni sohbet">
                  <i class="material-icons">speaker_notes</i>
                </button></div>
              <div class="menu-item">
                <button class="icon" title="Menü">
                  <i class="material-icons">more_vert</i>
                </button></div>
            </div>
          </div>
        </header>
        SideBar
      </div>
      <div id="main" class="pane pane-two">Container</div>

    </div>

  </div>
</template>

<script>
  export default {
    name: 'app',
    data() {
      return {
        msg: 'Welcome to Your Vue.js App',
        loading: true
      }
    },
    created() {
      setTimeout(() => {
        this.loading = false;
        console.log(this.loading)
      }, 1000);
    }

  }
</script>

<style lang="scss">
  @import "assets/styles/scss/app"
</style>