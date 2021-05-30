<template>
  <div id="app">
    <div class="row justify-content-between align-items-center">
      <div class="col-auto">
        <img alt="Vue logo" src="./assets/Logo.png" width="200" />
      </div>
      <div class="col-auto">
        <div id="nav" class="row align-items-center">
          <div class="col-auto">
            <router-link to="/"> Home </router-link> 
          </div>
          <div class="col-auto">
            <router-link to="/about"> About </router-link>
          </div>
        </div>
      </div>
    </div>
    <div class="row h-75 align-items-center">
      <router-view/>
    </div>
  </div>
</template>

<style lang="scss">
@import url("./assets/style.scss");

#nav {
  padding: 30px;

  a {
    color: var(--ligth);
    position: relative;
    z-index: 2;
    display: inline-block;
    line-height: 1.5;
    text-align: center;
    text-decoration: none;
    vertical-align: middle;
    cursor: pointer;
    -webkit-user-select: none;
    -moz-user-select: none;
    user-select: none;
    padding: 0.375rem 0.75rem;
    font-size: 1rem;
    font-weight: lighter;
    border-radius: 0.25rem;
    transition: color 0.15s ease-in-out, background-color 0.15s ease-in-out,
      border-color 0.15s ease-in-out, box-shadow 0.15s ease-in-out,
      transform 0.15s ease-in-out;

    &.router-link-exact-active {
      font-weight: bold;
    }

    &:hover {
      color: var(--color);
      background-color: var(--light);
      opacity: .9;
      border-color: var(--light);
      box-shadow: 3px 5px 5px rgba(0, 0, 0, 0.1);
      transform: scale(1.02);
    }
  }
}

</style>
