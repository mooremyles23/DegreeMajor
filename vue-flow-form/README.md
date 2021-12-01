# Vue Flow Form

Create conversational conditional-logic forms with Vue.js.

<p>
 
</p>

<p align="center">
 
</p>

## Demo

* [Questionnaire example](https://www.ditdot.hr/demo/vff/questionnaire/)

## Project Documentation

* [Guide](https://www.ditdot.hr/en/docs/vue-flow-form-guide)

## Example Project



To add Vue Flow Form as a dependency to your Vue project, use the following:

```shell
$ npm install @ditdot-dev/vue-flow-form --save
```

And then in your App.vue file:

```html
<template>
  <flow-form v-bind:questions="questions" v-bind:language="language" />
</template>

<script>
  // Import necessary components and classes
  import FlowForm, { QuestionModel, QuestionType, ChoiceOption, LanguageModel } from '@ditdot-dev/vue-flow-form'

  export default {
    name: 'example',
    components: {
      FlowForm
    },
    data() {
      return {
        language: new LanguageModel({
          // Your language definitions here (optional).
          // You can leave out this prop if you want to use the default definitions.
        }),
        questions: [
          // QuestionModel array
          new QuestionModel({
            title: 'Question',
            type: QuestionType.MultipleChoice,
            options: [
              new ChoiceOption({
                label: 'Answer'
              })
            ]
          })
        ]
      }
    }
  }
</script>

<style>
  /* Import Vue Flow Form base CSS */
  @import '~@ditdot-dev/vue-flow-form/dist/vue-flow-form.css';
  /* Import one of the Vue Flow Form CSS themes (optional) */
  @import '~@ditdot-dev/vue-flow-form/dist/vue-flow-form.theme-minimal.css';
  @import '~@ditdot-dev/vue-flow-form/dist/vue-flow-form.theme-green.css';
  @import '~@ditdot-dev/vue-flow-form/dist/vue-flow-form.theme-purple.css';
</style>
```

## Usage with plain JavaScript via CDN

HTML:

```html
<html>
  <head>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/vue/2.2.6/vue.min.js"></script>
    <!-- Flow Form -->
    <script src="https://unpkg.com/@ditdot-dev/vue-flow-form@1.1.0"></script>
    <!-- Flow Form base CSS -->
    <link rel="stylesheet" href="https://unpkg.com/@ditdot-dev/vue-flow-form@1.1.0/dist/vue-flow-form.min.css">
    <!-- Optional theme.css -->
    <link rel="stylesheet" href="https://unpkg.com/@ditdot-dev/vue-flow-form@1.1.0/dist/vue-flow-form.theme-minimal.min.css">
  </head>
  <body>
    <div id="app">
      <flow-form v-bind:questions="questions" v-bind:language="language" />
    </div>
    <script src="app.js"></script>
  </body>
</html>
```

JavaScript (content of app.js):

```js
var app = new Vue({
  el: '#app',
  data: function() {
    return {
      language: new FlowForm.LanguageModel({
        // Your language definitions here (optional).
        // You can leave out this prop if you want to use the default definitions.
      }),
      questions: [
        new FlowForm.QuestionModel({
          title: 'Question',
          type: FlowForm.QuestionType.MultipleChoice,
          options: [
            new FlowForm.ChoiceOption({
              label: 'Answer'
            })
          ]
        })
      ]
    }
  }
});
```
## Browser Support

Modern browsers and IE11.

## Changelog

Changes for each release are documented in the [release notes](https://github.com/ditdot-dev/vue-flow-form/releases).

## License

[MIT](https://github.com/ditdot-dev/vue-flow-form/blob/master/LICENSE) license.
