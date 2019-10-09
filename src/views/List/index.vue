<template>
  <div id="list">
    <h1>list List</h1>
    <ul>
        <li v-for="item in todos" v-bind:key="item" >
            {{ item.text }}
        </li>
    </ul>
  </div>
</template>

<script>
    export default{
        data(){
            return {
                todos: [
                    { text: '学习 JavaScript' },
                    { text: '学习 Vue' },
                    { text: '整个牛项目' }
                ]
            }
        }
    }
</script>

<style>

</style>script>
