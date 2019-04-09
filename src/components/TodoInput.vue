<template>
  <div class="todo-list__input">
        <input 
        :value="value"
        type="text" 
        @input="hanleInput"
        class="todo-list__input-textfield">
        <button 
        class="todo-list__input-button" 
        type="button"
        >
        Create
        </button>
      </div>
</template>

<script>
import { Stream } from 'stream';
export default {
name: 'TodoInput',
props:{
  value:{
    type: String
   }
  },
  methods:{
    hanleInput (event){
      this.$emit('input', event.target.value)
    }
  }
}
</script>

<style lang='scss'>
.todo-list{
  padding: 30px 15px;
  &__item{
    list-style: none;
    padding: 0;
    margin: 0;
  }
  &__list{
    width: 100%;
    border: 1px solid #000;
    border-radius: 10px;
    padding: 15px;
  }
&__input{
    display: flex;
    width: 100%;
    border: 1px solid #000;
    border-radius: 10px;
    padding: 2px;
  &-textfield{
   width: 100%;
   padding: 15px 0;
   margin-right: 15px;
   font-size: 18px;
   border: 0;
   outline: 0;
  }
  &-button{
    border: 0;
    border-radius: 30px;
    background-color: blue;
    color: antiquewhite;
    padding: 7.5px 30px;
    font-size: 14px;
    outline: 0;

    &:hover{
      color: #000;
    }
    }
  }
}
</style>
