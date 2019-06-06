<template>
  <div id="app">
    <b-navbar toggleable="lg" type="dark" variant="dark">
      <b-navbar-brand>
        <img src="./assets/sap-logo.png">
      </b-navbar-brand>
      <b-nav-text style="color:white;">
        <b>Dev Central</b>
      </b-nav-text>
    </b-navbar>
    <WorkspaceManager @parentCreateWs="createWs" v-if="wsm"/>
    <CreateWorkspace v-else/>
  </div>
</template>


<script>
import WorkspaceManager from "./components/WorkspaceManager";
import CreateWorkspace from "./components/CreateWorkspace";

export default {
  name: "app",
  components: {
    WorkspaceManager,
    CreateWorkspace
  },
  data() {
    return {
      wsm: true
    };
  },
  methods: {
    createWs() {
      this.$emit("parentCreateWs");
      this.wsm = false;
    }
  }
};
</script>

<style>
html,
body {
  height: 100%;
}

.flex-fill {
  flex: 1;
}

/* .row{
    display: flex;
} */

#app {
  height: 100%;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
