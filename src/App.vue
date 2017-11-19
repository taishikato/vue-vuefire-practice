<template>
  <div id="app" class="container">
    <div class="page-header">
      <h1>Vue.js 2 & Firebase Sample Application</h1>
    </div>
    <div class="panel panel-default">
      <div class="panel-heading">
        <h3>Books List</h3>
      </div>
      <div class="panel-body">
        <table class="table table-striped">
          <thead>
          </thead>
        </table>
      </div>
    </div>
  </div>
</template>

<script>
import Firebase from 'firebase'

const config = {
  apiKey: "AIzaSyCexpTR2SQ-AuvbVkZbIzg68brSED8-U6w",
  authDomain: "vue-firebase-dc79a.firebaseapp.com",
  databaseURL: "https://vue-firebase-dc79a.firebaseio.com",
  projectId: "vue-firebase-dc79a",
  storageBucket: "vue-firebase-dc79a.appspot.com",
  messagingSenderId: "885067538141"
}

const app = Firebase.initializeApp(config);
const db  = app.database();

const bookRef = db.ref('books');

export default {
  name: 'app',
  firebase: {
    books: bookRef
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
