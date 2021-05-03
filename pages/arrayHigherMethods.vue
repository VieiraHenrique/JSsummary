<template>
  <div class="ArrayMethods">
    <v-expansion-panels light>
      <v-expansion-panel v-for="(method, i) in methods" :key="i">
        <v-expansion-panel-header>
          <h3>{{ method.title }}</h3>
        </v-expansion-panel-header>
        <v-expansion-panel-content>
          <p v-html="method.content"></p>
          <a :href="method.link" target="blank">See MDN docs</a>
          <a :href="method.video" target="blank">See video</a>
        </v-expansion-panel-content>
      </v-expansion-panel>
    </v-expansion-panels>
  </div>
</template>

<script>
export default {
  data() {
    return {
      methods: [
        {
          title: 'forEach()',
          content:
            '<p>Takes a callback function that is applied to each element of the array.</p> <p>First parameter is the indivual element for each instance of the loop. Second parameter is the index.</p><p>The returned value can mutate the original array</p><code>array.forEach((element)=>{action})</code>',
          link:
            'https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/forEach',
          video:
            'https://www.udemy.com/course/javascript-beginners-complete-tutorial/learn/lecture/17010222#overview',
        },
        {
          title: 'map()',
          content: `<p>Returns a new array from the fonction you pass for each element of the original array.</p> <p>It's like a forEach that returns a new array and doesn't change the original array.</p><code>array.map((element)=>{
              return elementWithSomeAction
              })</code>`,
          link:
            'https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map',
          video:
            'https://www.udemy.com/course/javascript-beginners-complete-tutorial/learn/lecture/17010224#overview',
        },
        {
          title: 'find()',
          content: `<p>The find() method returns the value of the first element in an array that pass a test (provided as a function).</p><code>array.find((element)=>{
              return condition
              })</code>`,
          link:
            'https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/find',
          video:
            'https://www.udemy.com/course/javascript-beginners-complete-tutorial/learn/lecture/17010240#overview',
        },
        {
          title: 'filter()',
          content: `<p>Returns a new array with all elements that passed the test implemented by the provided function</p><code>array.filter((element)=>{
              return condition
              })</code>`,
          link:
            'https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter',
          video:
            'https://www.udemy.com/course/javascript-beginners-complete-tutorial/learn/lecture/17010242#overview',
        },
        {
          title: 'some()',
          content: `<p>Takes a test function and verify if at least one element of the array passes the test. Returns a boolean value.</p><code>array.some((element)=>{
              return condition
              })</code>`,
          link:
            'https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/some',
          video:
            'https://www.udemy.com/course/javascript-beginners-complete-tutorial/learn/lecture/17010244#overview',
        },
        {
          title: 'every()',
          content: `<p>Takes a test function and verify if every element of the array passes the test. Returns a boolean value.</p><code>array.some((element)=>{
              return condition
              })</code>`,
          link:
            'https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/every',
          video:
            'https://www.udemy.com/course/javascript-beginners-complete-tutorial/learn/lecture/17010244#overview',
        },
        {
          title: 'sort() - with callback',
          content: `<p>Takes a test function and verify if every element of the array passes the test. Returns a boolean value.</p><code>array.sort((a,b)=>{
              return a - b
              })</code>`,
          link:
            'https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/sort',
          video:
            'https://www.udemy.com/course/javascript-beginners-complete-tutorial/learn/lecture/17010248#overview',
        },
        {
          title: 'reduce()',
          content: `<p>Apply a function fn against an accumulator and each value (from right to left) of the array as to reduce it to a single value</p><code>array.reduce(function)</code>`,
          link:
            'https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/reduce',
          video:
            'https://www.udemy.com/course/javascript-beginners-complete-tutorial/learn/lecture/17010250#overview',
        },
      ],
    }
  },
}
</script>

<style>
h3 {
  color: rgb(22, 125, 209);
}
a {
  font-size: 14px;
  display: block;
}
code {
  color: red;
}
</style>
