<template>
  <div id="list">
    <h1>list {{msg}}</h1>
    <input type="text" v-model="msg">
    <ul class="bannerBox">
        <el-carousel>
            <el-carousel-item v-for="(item, i) in todos" :key="i">
                <div>
                    <img :src="item.linkData.linkPicUrl" alt="">
                </div>
            </el-carousel-item>
        </el-carousel>
    </ul>
    <div @click="handleClick" >click</div>
  </div>
</template>

<script>
    import axios from 'axios'
    export default{
        data(){
            return {
                todos: [],
                msg: '帅气'
            }
        },
        created() {
            this.hahah()
        },
        methods: {
            handleClick () {
                this.msg = this.msg + '10086'
            },
            hahah() {
                axios({
                    url: 'http://mapi.alkun.top/cms_list_tag?nid=23831003&type=2006&pageNo=0&pageSize=10'
                }).then(resp => {
                    console.log(resp)
                    this.todos = resp.data.result.results
                })
            }
        }
    }
</script>

<style>
    .bannerBox{
        width: 750px;
    }
    li {
        list-style: none;
        text-align: left;
    }

</style>
