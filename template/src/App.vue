/* @flow
<template>
  <div id="app">
    <img src="./assets/logo.png">
    {{#router}}
    <router-view></router-view>
    {{else}}
    <hello></hello>
    {{/router}}
  </div>
</template>
*/

// <script>
import Vue from 'vue'{{#if_eq lintConfig "airbnb"}};{{/if_eq}}
import Component from 'vue-class-component'{{#if_eq lintConfig "airbnb"}};{{/if_eq}}
{{#unless router}}
import Hello from './components/Hello'{{#if_eq lintConfig "airbnb"}};{{/if_eq}}
{{/unless}}

// flow can't check decorator currently
@Component({
  name: 'app'{{#if_eq lintConfig "airbnb"}},{{/if_eq}}
})
export default class App extends Vue {
  foo () {
    // $FlowFixMe
    this.$data(){{#if_eq lintConfig "airbnb"}};{{/if_eq}}
  }
  {{#unless router}}
  components: {
    Hello{{#if_eq lintConfig "airbnb"}},{{/if_eq}}
  }{{/unless}}
}{{#if_eq lintConfig "airbnb"}};{{/if_eq}}
// .</script>

/*
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
*/
