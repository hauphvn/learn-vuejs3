<script setup>
import HelloWorld from './components/HelloWorld.vue'
import TheWelcome from './components/TheWelcome.vue'
</script>

<template>
<!--  <header>-->
<!--    <img alt="Vue logo" class="logo" src="./assets/logo.svg" width="125" height="125" />-->

<!--    <div class="wrapper">-->
<!--      <HelloWorld msg="You did it!" />-->
<!--    </div>-->
<!--  </header>-->

<!--  <main>-->
<!--    <TheWelcome />-->
<!--  </main>-->
<!--  <div>{{greet}} {{name}}</div>-->
<!--  <br/>-->
<!--  <div v-text="gender"></div>-->
<!--&lt;!&ndash;  <hr>&ndash;&gt;-->
<!--  <div v-html="name"></div>-->
<!--&lt;!&ndash;  <div v-text="name">Hello</div>&ndash;&gt;-->
<!--  <h2 v-bind:id="headingId">heading id</h2>-->
<!--  <button v-bind:disabled="btnDisable">btn bind disable</button>-->
<!--  <p v-bind:class="statusClass">status class binding</p>-->
<!--  <div v-bind:class="{-->
<!--    underline: true,-->
<!--    danger: statusClass === 'danger' ? true : false-->
<!--  }">class array object</div>-->
<!--  <div v-bind:style="{-->
<!--    color: styleOrangeColor,-->
<!--    fontSize: sizeStyle + 'px'-->
<!--  }">style color</div>-->
<!--  <div v-bind:style="styleObj">style obj</div>-->
<!--  <div v-bind:style="[baseStyleObj, successStyleObj]">array style obj</div>-->
<!--  <div :style="[baseStyleObj, successStyleObj]">array style obj shorthand</div>-->
<!--  <div v-if="number === 0">number zero</div>-->
<!--  <div v-else-if="number < 0">negative number</div>-->
<!--  <div v-else-if="number > 0">positive number</div>-->
<!--  <div v-else>not zero</div>-->
<!--  <br>-->
<!--  <div v-if="display">-->
<!--    <p>display via v-if</p>-->
<!--  </div>-->
<!--  <div v-show="display">-->
<!--    <p>display via v-show is still on dom</p>-->
<!--  </div>-->
<!--  <br>-->
<!--  <div>-->
<!--    <p>render list</p>-->
<!--    <div v-for="student in students" :key="student.id">{{student.name}}</div>-->
<!--  </div>-->
<!--  <br>-->
<!--  <div>my info</div>-->
<!--  <div v-for="(value, key, index) in myInfo" :key="index">{{index}} {{key}} {{value}}</div>-->
<!--  <br>-->
<!-- <template>-->
<!--   <div>methods</div>-->
<!--   <div>{{add()}}</div>-->
<!--   <div>multiplier: {{mul(6)}}</div>-->
<!--  <div>{{fullName}}</div>-->
<!--  <button v-on:click="changeName('hau 2')">Change name</button>-->
<!--  <br>-->
<!--  <button @mouseover="changeName('hau 2',$event)">Change name shorthand</button>-->
<!-- </template>-->
  <div class="form-wrapper">
    <div class="control">
      <label for="username">Username</label>
      <input id="username" v-model="loginForm.username" type="text">
      <br>
      <label for="pwd">Password</label>
      <input id="pwd" v-model="loginForm.pwd" type="password">
      <div>
        <label for="country">Country</label>
        <select name="" v-model="loginForm.country" id="country">
          <option value="">Select a country</option>
          <option value="india">India</option>
          <option value="vietnam">Vietnam</option>
          <option value="singapore">Singapore</option>
        </select>
        <label for="country">CountryMulti</label>
        <select multiple name="" v-model="loginForm.countryMulti" id="country">
          <option value="">Select a country</option>
          <option value="india">India</option>
          <option value="vietnam">Vietnam</option>
          <option value="singapore">Singapore</option>
        </select>
      </div>
    </div>
    <div class="control">
      {{JSON.stringify(loginForm)}}
    </div>
  </div>
</template>
<script>
export default {
  name: 'App',
  data() {
    return {
      greet: 'hello',
      name: '<div style="color: green">hauphvn</div>',
      gender: 'nam',
      headingId: 'headingId',
      btnDisable: true,
      statusClass: 'danger',
      underlineClass: 'underline',
      styleOrangeColor: 'orange',
      sizeStyle: 20,
      styleObj: {
        color: 'blue',
        fontSize: '20px'
      },
      baseStyleObj: {
        fontSize: '50px',
        padding: '10px'
      },
      successStyleObj: {
        padding: '20px',
        border: '1px solid green',
        backgroundColor: 'lightgreen',
        color: 'green'
      },
      number: 10,
      display: false,
      students: [{
        id: 1,
        name: 'student 1'
      },
        {
          id: 2,
          name: 'student 2'
        },
        {
          id: 3,
          name: 'student 3'
        }],
      myInfo: {
        name: 'hauphvn',
        channel: 'hauChannel',
        course: 3
      },
      baseMultiplier: 5,
      fullName: 'pham van hau',
      loginForm: {
        username: '',
        pwd: '',
        country: '',
        countryMulti: []
      }
    };
  },
  methods: {
    add() {
      return 4 + 4;
    },
    mul(num) {
      return num * this.baseMultiplier;
    },
    changeName(newName, event) {
      console.log('event: ', event)
      this.fullName = newName;
    }
  }
}
</script>
<style scoped>
.danger {
  background-color: lightgoldenrodyellow;
  color: darkred;
}
.underline {
  text-decoration: underline;
}
.form-wrapper{
  display: grid;
  grid-template-columns: 1fr;
  background-color: antiquewhite;
  gap: 10px;
}
</style>
