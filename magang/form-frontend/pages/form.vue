<template>
<div class="container-fluid">
  <div class="container">
    <!-- Judul Form -->
    <div class="margin-top-bottom box question-box" id="form-head">
            <div class="form-title-box">
                <input type="text" class="form-title edit-on-click input-form-title txt-clr" v-model="form_title">
            </div>
            <textarea class="form-description edit-on-click textarea-adjust txt-clr" rows="1" placeholder="Form description" spellCheck = "false" v-model="form_title_description"></textarea>
    </div>
     <!-- Pertanyaan Form -->
    <div class="margin-top-bottom box question-box question">
      <input type="text"  class="question-title edit-on-click input-question " v-model="question_title">
      <select class="question-type-select input-question-type" v-model="selected">
          <option>Short answer</option>
          <option>Paragraph</option>
          <option>Multiple choice</option>
          <option>Checkbox</option>
      </select>
      <!-- If Short Answer -->
      <div class="answers" v-if="selected=='Short answer'">
          <input type ="text" class="short-answer" placeholder="Short answer text" />
      </div>
      <!-- If Paragraph -->
      <div class="answers" v-if="selected=='Paragraph'">
          <textarea class="long-answer" placeholder="Long answer text" ></textarea>
      </div>
      <!-- If Multiple choice -->
      <div class="answers" v-if="selected=='Multiple choice'">
        <span>**Pertanyaan Multiple choice belum dibuat**</span>
        <div id="todo-list-example">
          <form v-on:submit.prevent="addNewTodo">
            <label for="new-todo">Add a todo</label>
            <input
              v-model="newTodoText"
              id="new-todo"
              placeholder="E.g. Feed the cat"
            >
            <button>Add</button>
          </form>
          <ul>
            <li
              is="todo-item"
              v-for="(todo, index) in todos"
              v-bind:key="todo.id"
              v-bind:title="todo.title"
              v-on:remove="todos.splice(index, 1)"
            ></li>
          </ul>
        </div>
      </div>
      <div class="answers" v-if="selected=='Checkbox'">
        <span>**Pertanyaan Checkbox belum dibuat**</span>
      </div>
    </div>
  </div>
</div>
</template>
<script>
export default {
  name: 'FormPage',
  data () {
    return {
      form_title: 'Untitled Form',
      question_title: 'Untitled Question',
      selected: 'Short answer'
    }
  }
}
</script>

<style scoped>
body {
  font-family: Roboto, Oxygen, Ubuntu, Cantarell, "Open Sans", "Helvetica Neue",sans-serif;
}
.box{
  padding: 10px;
  border: 1px solid #999;
  border-radius: 5px;
  width: -webkit-fill-available;
  width: -moz-available;
  margin: 20px 0px;
}
.question-box{
  background-color: white;
}
.form-title-box{
    border-bottom: 1px solid #ddd;
}
.form-title{
    border: none;
    font-size: 2rem;
    font-family: "Roboto Condensed";
    font-weight: normal;
    margin: 10px;
    width: -webkit-fill-available;
    width: -moz-available;
}
.form-description{
    border: none;
    font-size: 1rem;
    font-family: "Roboto Condensed";
    margin: 10px;
    width: -webkit-fill-available;
    width: -moz-available;
}
.question-title{
    border: none;
    font-family: "Roboto Condensed";
    font-size: 1.5rem;
    width: 65%;
}
.question-type-select{
    width: calc(35% - 8px);
    padding: 5px 35px 5px 5px;
    font-size: 1.2rem;
    border: 1px solid #ccc;
    height: 34px;
}
.answers{
    margin: 5px;
    font-family: "Google Sans";
}

.short-answer{
    width: 50%;
    border: none;
    padding: 5px;
    border-bottom: 1px solid #70757a;
}

.long-answer{
    width: -webkit-fill-available;
    width: -moz-available;
    border: none;
    padding: 5px;
    border-bottom: 1px solid #70757a;
}
</style>
