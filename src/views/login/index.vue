<template>
  <div>

    <div>

      <div class="login">
        <div class="title">
          live
        </div>

        <div class="ipt">
          <el-input v-model="num" placeholder="请输入账号"></el-input>
          <el-input v-model="pswd" placeholder="请输入密码" style="margin-top:2vh"></el-input>
        </div>


        <div :class="btn==true?'btn':'btns'" @click="login()">登陆</div>
      </div>


      <video autoplay="autoplay" loop="loop" muted="muted" controlsList="nodownload" class="aaa">
        <source src="http://47.103.40.123:8080/static/media/bgvide.13edb8ad.mp4" type="video/mp4" />
      </video>

    </div>
  </div>



</template>

<script>
  export default {
    data() {
      return {
        num: '',
        btn:true
      }
    },
    methods:{
      login(){
        this.btn=false
        setTimeout(()=>{
          this.btn=true
        },50)
      }
    }
  }
</script>

<style lang="scss">
  * {
    padding: 0;
    margin: 0;
    overflow-y: hidden
  }

  .aaa {
    position: absolute;
    top: 0;
    width: 100%;
    height: 100vh;
    background: linear-gradient(to right, #8eaeb3, #aac4c8, #8eaeb3);
  }

  .login {
    width: 60vh;
    height: 30vh;
    position: absolute;
    background-color: rgba(255, 255, 255, .3);
    left: 25%;
    top: 40%;
    z-index: 99;

    .title {
      width: 100%;
      text-align: center;
      font-size: 4vh;
      color: #8eaeb3;
    }

    .ipt {
      width: 80%;
      height: 16vh;
      margin: 0 auto;
    }

    .btn {
      width: 80%;
      height: 6vh;
      background-color: #8eaeb3;
      margin: 0 auto;
      font-size: 3vh;
      line-height: 6vh;
      color: #fff;
      text-align: center;
    }
    .btns{
       width: 80%;
      height: 6vh;
      background-color: #aac4c8;
      margin: 0 auto;
      font-size: 3vh;
      line-height: 6vh;
      color: #fff;
      text-align: center;
    }

    
  }
  .btn:hover {
      cursor: pointer
    }
</style>