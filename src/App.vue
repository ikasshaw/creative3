<template>
  <div id="app">
    <div class="allExceptFooter">
      <div id="menu">
        <div id="brand">
          <router-link to="/">
            <img src="../public/images/f1.png" />
          </router-link>
        </div>
        <div id="bottom">
          <router-link to="/teams">
            <div class="menu-item browse">
              <p>TEAMS</p>
            </div>
          </router-link>
          <router-link to="/drivers">
            <div class="menu-item">
              <p>DRIVERS</p>
            </div>
          </router-link>
        </div>
      </div>
      <router-view />
    </div>
    <footer>
      <a target="_blank" href="https://github.com/ikasshaw/creative3.git"
        ><img src="../src/assets/GitHub-Mark-120px-plus.png" alt="Github icon"
      /></a>
    </footer>
  </div>
</template>

<script>
export default {
  name: 'App',
};
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Montserrat:ital,wght@0,400;0,700;1,400;1,700&family=Roboto:ital,wght@0,400;0,700;1,400;1,700&display=swap');

* {
  box-sizing: border-box;
  font-family: 'Roboto', 'Montserrat', 'Open Sans', 'Helvetica Neue', sans-serif;
}

#app {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}

.allExceptFooter {
  padding-bottom: 100px;
  /*margin: 50px 100px 0 100px;*/
}

#menu {
  display: flex;
  flex-direction: column;
  padding: 0 10px 0 10px;
  margin: 5px 5px 65px 5px;
}

#menu a {
  text-decoration: none;
}

#brand {
  grid-area: brand;
  display: flex;
  justify-content: center;
  padding-bottom: 30px;
}

#brand img {
  height: 75px;
}

#bottom {
  width: 100%;
  display: flex;
  justify-content: space-around;
}

.menu-item {
  display: flex;
  flex-direction: column;
  color: red;
  font-size: 1.75em;
}

.menu-item p {
  margin: 0;
}

footer {
  background-color: #292f3633;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 15px 0 15px 0;
  margin-top: auto;
}

footer a {
  text-decoration: none;
}

footer a img {
  max-width: 30px;
}
</style>
