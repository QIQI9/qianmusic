<template>
    <div class="head-box">
        <div class="box">
            <div class="pag">
            <div class="fl">
                <img src="https://static1-qianqian.91q.com/client/img/3713308.png" alt="">
                <a href="javascript:;">立即登录</a>
            </div>
            <div class="fr">
                <div class="fr-l">
                    <div>开通会员，立享特权</div>
                    <button>立即开通</button>
                </div>
            </div>
        </div>
        </div>
        <div class="conta">
            <div class="gro">
                <div>会员特权</div>
            </div>
            <div class="vip">
                <div class="p1">
                    <div class="item">
                        <img src="../assets/1.png" alt="">
                        <div class="name">VIP曲库</div>
                        <div class="into">独享更多VIP专属曲库内容（不含数字专辑）</div>
                    </div>
                    <div class="item">
                        <img src="../assets/1.png" alt="">
                        <div class="name">VIP曲库</div>
                        <div class="into">独享更多VIP专属曲库内容（不含数字专辑）</div>
                    </div>
                    <div class="item">
                        <img src="../assets/1.png" alt="">
                        <div class="name">VIP曲库</div>
                        <div class="into">独享更多VIP专属曲库内容（不含数字专辑）</div>
                    </div>
                </div>
            </div>
        </div>
        <div class="gro1">
            <div class="title">-会员歌单-</div>
                <div class="lll">
                    <div class="pos" v-for="(item,index) in arrs" :key="index">
                    <div class="imga">
                        <img :src="item.imgsrc" alt="">
                    </div>
                    <div class="name">{{item.title}}</div>  
                </div>
                <div class="con">

                </div>
            </div>
            
        </div>
    </div>
</template>
<script>
import axios from "axios"
export default {
    name:"VIP",
    data(){
        return {
            arrs:null
        }
    },
    component:{},
    components:{},
    methods: {
      async aaa(){
        let {data} =await axios.get("http://localhost:3000/arrs")
        console.log(data)
        this.arrs=data
       }
    },
    watch:{},
    created() {
        this.aaa()
    },
    
}
</script>

<style scoped>

    .head-box{
        margin-top: 50px;
        margin: auto;
    }
    .box{
        background: #333;
        width: 1349px;
        height: 300px;
      
    }
    .pag{
        display: flex;
        justify-content: space-around;
        padding-top: 50px;
    }
    .fr{
        width: 680px;
        height: 250px;
        background: url(https://static1-qianqian.91q.com/client/img/f09046e.png);
    }
    .fl{
        margin-top: 65px;
        display: flex;
        align-items: center;
    }
    .fl>a{
        margin-left: 30px;
        text-decoration: none;
        color:white;
    }
    .fl>img{
        width: 120px;
        height: 120px;
    }
    .fr>.fr-l>div{
        font-size: 36px;
    }
    .fr>.fr-l{
        padding: 0 60px;
        margin-top: 65px;
    }
    .fr>.fr-l>button{
        padding: 17px 40px;
        border-radius: 25px;
        background: #333;
        margin-top: 25px;
    }
    .conta{
    width: 1200px;
    margin: 0 auto;
  }
  .conta>.gro>div{
        margin: 100px 0 40px;
        text-align: center;
        font-size: 28px;

  }
  .conta>.vip>.p1{
      display: flex;
      justify-content: space-around;
  }
  .conta>.vip>.p1>.item{
    display: flex;
    flex-direction: column;
    justify-content: center;
   
    width: 380px;
    height: 255px;
    padding: 50px 0;
    text-align: center;
    background: #f8f8f8;
  }
  .conta>.vip>.p1>.item>img{
      width: 80px;
      height: 80px;
      margin-left: 145px;
      margin-bottom: 20px;
  }
  .head-box>.gro1>.title{
        margin: 100px 0 40px;
        text-align: center;
        font-size: 28px;
  }
  .head-box>.gro1>.lll>.pos{
      width: 224px;
      height: 268px;
      margin: auto;
      margin: 25px 5px 0 0;
  }
  .head-box>.gro1>.lll{
      /* width: 1200px; */
      display: flex;
      /* margin: auto; */
      padding: 0 80px;
      flex-wrap: wrap;
      justify-content: space-between;
      margin-bottom: 20px;
  }
  .head-box>.gro1>.lll>.pos>.name{
    margin-top: 18px;
    font-size: 16px;
    height: 26px;
    line-height: 26px;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
  }
  .head-box>.gro1>.lll>.pos>.imga{
      width: 224px;
      height: 224px;
  }
  .con{
    content: "";
    display: block;
    width:224px;
}
  
</style>