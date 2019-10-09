<template>
  <div id="list">
    <h1>list {{msg}}</h1>
    <input type="text" v-model="msg">
    <ul>
        <li v-for="(item, i) in todos" :key="i" >
            {{ item.text }}
        </li>
    </ul>
    <div v-on:click="handleClick" >click</div>
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
                ],
                msg: '帅气'
            }
        },
        methods: {
            handleClick () {
                this.msg = this.msg + '10086'
            }
        }
    }
</script>

<style>

</style>
