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
          title: 'push()',
          content:
            '<p>Add element to end of array and return new length</p><code>array.push(element)</code>',
          link:
            'https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/push',
          video:
            'https://www.udemy.com/course/javascript-beginners-complete-tutorial/learn/lecture/16981328#overview',
        },
        {
          title: 'pop()',
          content:
            '<p>Remove and return last element from an array</p><code>array.pop()</code>',
          link:
            'https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/pop',
          video:
            'https://www.udemy.com/course/javascript-beginners-complete-tutorial/learn/lecture/16981328#overview',
        },
        {
          title: 'unshift()',
          content:
            '<p>Add element to start of array and return new length</p><code>array.unshift(element)</code>',
          link:
            'https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/unshift',
          video:
            'https://www.udemy.com/course/javascript-beginners-complete-tutorial/learn/lecture/16981330#overview',
        },
        {
          title: 'shift()',
          content:
            '<p>Remove first element of array and return the element</p><code>array.shift()</code>',
          link:
            'https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/shift',
          video:
            'https://www.udemy.com/course/javascript-beginners-complete-tutorial/learn/lecture/16981330#overview',
        },
        {
          title: 'concat()',
          content:
            '<p>Return new array by joining arrays array1 and array2 together</p><code>array1.concat(array2)</code>',
          link:
            'https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/concat',
          video:
            'https://www.udemy.com/course/javascript-beginners-complete-tutorial/learn/lecture/16981336#overview',
        },
        {
          title: 'includes()',
          content:
            '<p>Returns TRUE or FALSE if the Array includes an element.</p><code>array.includes(element)</code>',
          link:
            'https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/includes',
          video:
            'https://www.udemy.com/course/javascript-beginners-complete-tutorial/learn/lecture/16981338#overview',
        },
        {
          title: 'indexOf()',
          content: `<p>Returns the index of an elements of the Array. </br>
If it is not found, it returns -1</p><code>array.indexOf(element)</code>`,
          link:
            'https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/indexOf',
          video:
            'https://www.udemy.com/course/javascript-beginners-complete-tutorial/learn/lecture/16981338#overview',
        },
        {
          title: 'join()',
          content: `<p>Creates a string from an array. </br>
If no argument is passed, it's separated by a comma ( , ). Otherwise you can pass by what it will be joined.</br>
If it is not found, it returns -1</p><code>array.join('-')</code>`,
          link:
            'https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/join',
          video:
            'https://www.udemy.com/course/javascript-beginners-complete-tutorial/learn/lecture/16981344#overview',
        },
        {
          title: 'reverse()',
          content: `<p>Reverses an array. The original array is changed</p><code>array.reverse()</code>`,
          link:
            'https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/reverse',
          video:
            'https://www.udemy.com/course/javascript-beginners-complete-tutorial/learn/lecture/16981344#overview',
        },
        {
          title: 'slice()',
          content: `<p>Copy portion of an array. Returns a new array</p><p>It doesn't impact the orignal array.</p><p>It takes an index argument from when you want to copy the array and another to when you want to end. If you put 0, it will copy the whole array.</p><code>array.slice(startIndex, endIndex)</code>`,
          link:
            'https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/slice',
          video:
            'https://www.udemy.com/course/javascript-beginners-complete-tutorial/learn/lecture/16981350#overview',
        },
        {
          title: 'splice()',
          content: `<p>Remove / replace elements of an array. It changes the original array.</p><p>It returns the elements deleted.</p><p>It takes three arguments :</p><code>array.splice( where to begin , how many delete , what to insert)</code>`,
          link:
            'https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/splice',
          video:
            'https://www.udemy.com/course/javascript-beginners-complete-tutorial/learn/lecture/16981354#overview',
        },
        {
          title: 'sort()',
          content: `<p>Sorts an array by the first character (after converting it to a string).</p><p>Changes the original array</p><code>array.sort()</code>`,
          link:
            'https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/sort',
          video:
            'https://www.udemy.com/course/javascript-beginners-complete-tutorial/learn/lecture/16981360#overview',
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
