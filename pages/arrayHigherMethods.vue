<template>
  <div class="ArrayMethods">
    <v-expansion-panels light>
      <v-expansion-panel v-for="(method, i) in methods" :key="i">
        <v-expansion-panel-header>
          <h3>{{ method.title }}</h3>
        </v-expansion-panel-header>
        <v-expansion-panel-content>
          <p v-for="(p, i) in method.content" :key="i">
            {{ p }}
          </p>
          <code>{{ method.code }}</code>
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
          content: [
            'Takes a callback function that is applied to each element of the array.',
            'First parameter is the indivual element for each instance of the loop. Second parameter is the index.',
            'The returned value can mutate the original array',
          ],
          code: 'array.forEach((element)=>{action})',
          link:
            'https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/forEach',
          video:
            'https://www.udemy.com/course/javascript-beginners-complete-tutorial/learn/lecture/17010222#overview',
        },
        {
          title: 'map()',
          content: [
            'Returns a new array from the fonction you pass for each element of the original array.',
            `It's like a forEach that returns a new array and doesn't change the original array.`,
          ],
          code: 'array.map((element)=>{return elementWithSomeAction})',
          link:
            'https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map',
          video:
            'https://www.udemy.com/course/javascript-beginners-complete-tutorial/learn/lecture/17010224#overview',
        },
        {
          title: 'find()',
          content: [
            `The find() method returns the value of the first element in an array that pass a test (provided as a function).`,
          ],
          code: `array.find((element)=>{
              return condition
              })`,
          link:
            'https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/find',
          video:
            'https://www.udemy.com/course/javascript-beginners-complete-tutorial/learn/lecture/17010240#overview',
        },
        {
          title: 'filter()',
          content: [
            `Returns a new array with all elements that passed the test implemented by the provided function`,
          ],
          code: `array.filter((element)=>{
              return condition
              })`,
          link:
            'https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter',
          video:
            'https://www.udemy.com/course/javascript-beginners-complete-tutorial/learn/lecture/17010242#overview',
        },
        {
          title: 'some()',
          content: [
            `Takes a test function and verify if at least one element of the array passes the test. Returns a boolean value.`,
          ],
          code: `array.some((element)=>{
              return condition
              })`,
          link:
            'https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/some',
          video:
            'https://www.udemy.com/course/javascript-beginners-complete-tutorial/learn/lecture/17010244#overview',
        },
        {
          title: 'every()',
          content: [
            'Takes a test function and verify if every element of the array passes the test. Returns a boolean value.',
          ],
          code: `array.some((element)=>{
              return condition
              })`,
          link:
            'https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/every',
          video:
            'https://www.udemy.com/course/javascript-beginners-complete-tutorial/learn/lecture/17010244#overview',
        },
        {
          title: 'sort() - with callback',
          content: [
            `Takes a test function and verify if every element of the array passes the test. Returns a boolean value.`,
          ],
          code: `array.sort((a,b)=>{
              return a - b
              })`,
          link:
            'https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/sort',
          video:
            'https://www.udemy.com/course/javascript-beginners-complete-tutorial/learn/lecture/17010248#overview',
        },
        {
          title: 'reduce()',
          content: [
            `Apply a function fn against an accumulator and each value (from right to left) of the array as to reduce it to a single value`,
          ],
          code: `array.reduce(function)`,
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
  display: inline-block;
  margin-bottom: 20px;
}
</style>
