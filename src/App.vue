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
<!--  <div class="form-wrapper">-->
<!--    <input type="text" placeholder="call api init obj first" v-model="callAPIObj.first">-->
<!--    <input type="text" placeholder="call api init obj last" v-model="callAPIObj.last">-->
<!--    <input placeholder="typing for call api" type="text" v-model="callAPI">-->
<!--    <div>testGetSetOnComputed: {{ JSON.stringify(testGetSetOnComputed) }}</div>-->
<!--    <button @click="testGetSetOnComputed = {first: 'a1',last: 'b1'}">set value via computed</button>-->
<!--    <div>testWatch: {{ JSON.stringify(testWatch) }}</div>-->
<!--    <button @click="testWatch = {first: 'a1',last: 'b1'}">set value via watch</button>-->

<!--    <div>Using computed: Fullname: {{ fullNameComputed }}</div>-->
<!--    <div>Using method: Fullname Method: {{ methodFullName() }}</div>-->
<!--    <button @click="firstName = 'change first name'">change firstname to demonstrate computed</button>-->
<!--    <div v-pre>{{ changeOnce }}</div>-->
<!--    <div>{{ changeOnce }}</div>-->
<!--    <button @click="changeOnce +=1">change once</button>-->
<!--    <form @submit.prevent="submitForm">-->
<!--      <div class="control">-->
<!--        <label for="username">Username</label>-->
<!--        <input id="username" v-model.trim.lazy="loginForm.username" type="text">-->
<!--        <br>-->
<!--        <label for="pwd">Password</label>-->
<!--        <input id="pwd" v-model="loginForm.pwd" type="password">-->
<!--        <div>-->
<!--          <label for="country">Country</label>-->
<!--          <select name="" v-model="loginForm.country" id="country">-->
<!--            <option value="">Select a country</option>-->
<!--            <option value="india">India</option>-->
<!--            <option value="vietnam">Vietnam</option>-->
<!--            <option value="singapore">Singapore</option>-->
<!--          </select>-->
<!--          <label for="country">CountryMulti</label>-->
<!--          <select multiple name="" v-model="loginForm.countryMulti" id="country">-->
<!--            <option value="">Select a country</option>-->
<!--            <option value="india">India</option>-->
<!--            <option value="vietnam">Vietnam</option>-->
<!--            <option value="singapore">Singapore</option>-->
<!--          </select>-->
<!--        </div>-->
<!--      </div>-->
<!--      <button type="submit">submit</button>-->
<!--    </form>-->
<!--    <div class="control">-->
<!--      {{ JSON.stringify(loginForm) }}-->
<!--    </div>-->
<!--  </div>-->
<!--  <Greet id="hauphvn-id" name="hauphvn" :username="fullName"/>-->
<!--  <br>-->
<!--  <Greet :name="gender" username="userName" :likes=3 email="sdfsdf@gmail.com" />-->
<!--  <button @click="onClickPopup">Show popup</button>-->
<!--<div v-show="showPopup">-->
<!--  <Popup @close="onClosePopup" />-->
<!--</div>-->
<!--  <div v-if="!showPopup">-->
<!--    Data from popup: {{dataFromPopup}}-->
<!--  </div>-->
<!--  <br>-->
<!--  <SlotExample/>-->
<!--  <br>-->
<!--  <SlotExample>-->
<!--    <h2>Children of slot</h2>-->
<!--  </SlotExample>-->
<!--  <br>-->
<!--  <NamedSlot>-->
<!-- <template v-slot:content>-->
<!--   <h2>content</h2>-->
<!-- </template>-->
<!--  </NamedSlot>-->

<!--  listslot-->
<!--  <ListSlot>-->
<!--    <template v-slot:default="slotProps">-->
<!--      {{slotProps.email}}-->
<!--    </template>-->
<!--  </ListSlot>-->
<!--  <ListSlot>-->
<!--    <template v-slot:default="slotProps">-->
<!--      {{slotProps.username}} | {{slotProps.email}}-->
<!--    </template>-->
<!--  </ListSlot>-->
<!--  end listslot-->
<!--stylecompoent-->
<StyleComponent/>
  <StyleOtherComponent>
      <h4>h4 from app into slot other component</h4>
  </StyleOtherComponent>
  <div class="style-component-1">Style component of App</div>
  <h4>style app h4</h4>
<!--  end-style-component-->

</template>
<script>
import StyleComponent from "@/components/StyleComponent.vue";
import StyleOtherComponent from "@/components/StyleOtherComponent.vue";
import SlotExample from './components/SlotExample.vue';
import Popup from './components/Popup.vue';
import Greet from './components/Greet.vue';
import NamedSlot from "@/components/NamedSlot.vue";
import ListSlot from "@/components/ListSlot.vue";
export default {
  name: 'App',
  components: {
    ListSlot,
    Greet,
    Popup,SlotExample, NamedSlot, StyleComponent, StyleOtherComponent
  },
  data() {
    return {
      showPopup: false,
      dataFromPopup: '',
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
      },
      changeOnce: 1,
      firstName: 'hau',
      lastName: 'pham',
      testGetSetOnComputed: {
        first: 'a',
        last: 'b'
      },
      testWatch: {
        first: 'watch a',
        lats: 'watch b'
      },
      callAPI: 'call api init',
      callAPIObj: {
        first: '',
        last: ''
      }
    };
  },
  methods: {
    onClosePopup(event){
      this.dataFromPopup = event ? event : '';
     this.showPopup = false;
    },
    add() {
      return 4 + 4;
    },
    mul(num) {
      return num * this.baseMultiplier;
    },
    changeName(newName, event) {
      console.log('event: ', event)
      this.fullName = newName;
    },
    submitForm() {
      console.log(this.loginForm)
    },
    methodFullName() {
      console.log('method fullname')
      return `${this.firstName} ${this.lastName}`;
    },
    onClickPopup(){
     this.showPopup = true;
    }
  },
  computed: {
    fullNameComputed() {
      console.log('computed fullname')
      return `${this.firstName} ${this.lastName}`;
    },
    testGetSetOnComputed: {
      get() {
        console.log('get...')
        return `${this.testGetSetOnComputed.first} - ${this.testGetSetOnComputed.last}`;
      },
      set(newValue) {
        const { first, last } = newValue;
        console.log('set...');
        this.testGetSetOnComputed.first = first;
        this.testGetSetOnComputed.last = last;
      }
    }
  },
  watch: {
    testWatch(newValue, oldValue) {
      // console.log('call api')
    },
    callAPI: {
      handler(value) {
        console.log('value call api: ', value)
      },
      immediate: true
    },
    callAPIObj: {
      handler(value){
        console.log('call api obj: ', JSON.stringify(value))
      },
      deep: true
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

.form-wrapper {
  display: grid;
  grid-template-columns: 1fr;
  background-color: antiquewhite;
  gap: 10px;
}
.style-component-1{
  color: darkred;
}
h4{
  background-color: darkred;
  color: white;
}
</style>
