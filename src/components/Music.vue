<template>
    <!--只能存在一个根容器-->
    <div class="music">
      音乐实例
      <p class="p1" ref="p1">原生p元素</p>
      <input ref="myinput" type="text">
      <button @click="getValue" type="button">get</button>
    </div>
</template>

<script>
    export default {
        name: 'music',
        props: [],
        //所有的初始化状态全部放入data中
        data() {
            return {

            }
        },

        mounted(){
          console.log(this.$refs.p1)
          this.$refs.p1.innerHTML="改变吧！"
        },

        methods: {

          getValue(){
            console.log(this.$refs.myinput.value)
          }

        },
        //计算属性
        computed: {},

        //实时监听数据变化，可以在这里做相关判断
        watch: {}

    }
</script>

<!--样式-->
<!--
Add "scoped" attribute to limit CSS to this component only
添加scoped属性限制样式只在当前组件中生效
-->
<style>

</style>
