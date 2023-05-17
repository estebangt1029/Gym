<template>
        <nav>
            <a href="/">Gym</a>
            <input type="checkbox">
            <div class="menu">
                <RouterLink to="/">Inicio</RouterLink>
                <RouterLink to="/entrenadores">Entrenadores</RouterLink>
            </div>
        </nav>
</template>

<style scoped>
  nav{
    position: fixed;
    z-index: 1;
    top: 0;
    width: 100vw;
    height: 60px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0 2rem;
    background: -webkit-linear-gradient(-73deg, rgb(255, 255, 255), rgb(0, 0, 0));
    background: linear-gradient(-73deg, rgb(255, 255, 255), rgb(0, 0, 0));
  }
  .menu {
    position: fixed;
    left: 0;
    top: 59px;
    height: 93vh;
    width: 100vw;
    display: none;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    background: -webkit-linear-gradient(19deg, rgb(0, 0, 0), rgb(255, 255, 255));
    background: linear-gradient(88deg, rgb(0, 0, 0), rgb(255, 255, 255));
    z-index: 1;
  }
  input{
    width: 30px;
    height: 30px;
    appearance: none;
    background-image: url(../assets/abrirmenu.png);
    background-repeat: no-repeat;
    background-size: cover;
    cursor: pointer;
  }
  input:checked{
    width: 30px;
    height: 30px;
    appearance: none;
    background-image: url(../assets/cerrarmenu.png);
    background-repeat: no-repeat;
    background-size: cover;
  }
  input:checked ~ .menu{
    display: flex;
  }
  a{
    position: relative;
    cursor: pointer;
    text-decoration: none;
    color: white;
    font-size: xx-large;
  }
  a:before{
    content: "";
    position: absolute;
    width: 0;
    left: 0;
    bottom: 0;
    height: 3px;
    background-color: white;
    transition: width .5s;
  }
  a:hover:before{
    width: 100%;
  }
  
</style>