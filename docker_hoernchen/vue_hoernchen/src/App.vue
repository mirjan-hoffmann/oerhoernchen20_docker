<template>
  <div id="app">
  <app-fork-me></app-fork-me>
  <!-- NavBar -->
  <app-nav-bar></app-nav-bar>

  <router-view></router-view>

  <button onclick="topFunction()" id="myBtn" title="Go to top"><font-awesome-icon icon="arrow-circle-up" /></button>

</div>
</template>

<script>
import NavBar from './components/NavBar.vue'
import SearchApp from './components/search/SearchApp'
import ForkMe from './components/ForkMe'

export default {
		name: 'App',
    components: {
      'app-nav-bar': NavBar,
      'app-search-app': SearchApp,
      'app-fork-me': ForkMe
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

#navbar{
	/*background-color: #6F1E51 !important;*/
}

a.navbar-brand{
	margin-left:10px;
	/*color:#C4E538 !important;*/
	/*font-size:25px;*/
  font-weight:800;
	font-family: 'Open Sans', sans-serif;
}

#navbar img{
	max-height: 45px;
}

#navbar a, #navbar a:visited{
	/*color:#C4E538 !important;*/
}

#navbar .navbar-toggler {
    /*color: #C4E538;
    border-color: #C4E538; */
}

/* https://codepen.io/SteveJRobertson/pen/POdvgz */

/* 2do: use container */

.result-list-container .card{
	margin-bottom:15px;
  box-shadow: 0 0 2px rgba(24, 28, 43, 0.2);
  /*border:none;*/
}
.result-list-container .card .card-footer{
  /*border:none;
  background:none;*/
}

.result-list-container .card h4{
	font-size:16px;
}

.result-list-container .card-text{
	font-size:14px;
}

.result-list-container a:visited,.result-list-container a{
	color:#333;
}

/*.card-horizontal {
    display: flex;
    flex: 1 1 auto;
}*/

.thumbnail{
	width:150px;
	margin-left:10px;
	margin-bottom: 10px;
}


.filter {
  background: white;
  padding: 10px;
  margin: 10px 0;
  box-shadow: 0 0 2px rgba(24, 28, 43, 0.2);
  color: #181c2b;
}

.filters-container {
  /*display: flex;
  flex-direction: column;
  width: 25%;*/
  padding: 10px;
}

/* 2DO: change to mint green*/
.filter input:checked + label::before {
    /*border-color: #6F1E51;*/
    background-color: rgb(120, 194, 173);
}

.hiddenDetails {
  display: None
}

.result-list-container {
  margin: 10px;
  padding: 10px;
}

#myBtn {
  display: none; /* Hidden by default */
  position: fixed; /* Fixed/sticky position */
  bottom: 20px; /* Place the button at the bottom of the page */
  right: 30px; /* Place the button 30px from the right */
  z-index: 99; /* Make sure it does not overlap */
  border: none; /* Remove borders */
  outline: none; /* Remove outline */
  background-color: rgb(91, 91, 91); /* Set a background color */
  color: white; /* Text color */
  cursor: pointer; /* Add a mouse pointer on hover */
  padding: 15px; /* Some padding */
  border-radius: 10px; /* Rounded corners */
  font-size: 18px; /* Increase font size */
}

#myBtn:hover {
  background-color: #555; /* Add a dark-grey background on hover */
}
</style>