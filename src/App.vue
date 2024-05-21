<template>

<nav id="navbar">
        <h1>Randy Ivando</h1>
        <ul>
        <li><a href="#">Home</a></li> 
        <li><a href="#">Profile</a></li>
        <li><a href="#">About</a></li>
        <li><a href="#">Contact</a></li>
        </ul>
    </nav>
  <div id="app">
    <Emit />
  </div>
</template>

<script>
import Emit from './components/Emit.vue';

export default {
  components: {
    Emit,
  },
};
</script>

<style scoped>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
 
}

body {
  background-color: #e3e3e3;
}

#navbar h1 {
    --c:linear-gradient(#ff0000 0 0); /* update the color here */
  
    padding-bottom: .15em;
    background: var(--c), var(--c);
    background-size: .3em .1em;
    background-position:50% 100%;
    background-repeat: no-repeat;
    transition: .3s linear, background-size .3s .2s linear;
    color: #252525;
    margin-left: 20px;
    font-family:'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
    cursor: pointer;
}

#navbar h1:hover{
    background-size: 40% .1em;
    background-position: 10% 100%, 90% 100%;
}

#navbar{
    background-color: rgba(212, 180, 21, 0);
    display: flex; 
    justify-content: space-between;
}
#navbar ul {
    display: flex;
    list-style: none;
    align-items: center;
    gap: 1rem 2rem;
    margin-right: 30px;
}

#navbar ul li a {
    text-decoration: none;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    font-weight: 600;
    padding:  3px 0px;
    border-bottom: 2px solid rgba(255, 0, 0, 0);
    transition: all;
    transition-duration: 300ms;
    position: relative;
    color: #252525;
    cursor: pointer;
}


#navbar ul li a::before{
    content: '';
    position: absolute;
    top: 100%;
    left: 0;
    width: 0;
    height: 2.5px;
    background: red;
    transition: 0.3s;
}

#navbar ul li a:hover::before{
    width: 100%;
}

</style>
