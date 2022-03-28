<template>
  <div class="client-box">
    <div class="client-box-center content">
      <div class="center-qqh2">
        <p>千千音乐客户端</p>
      </div>
      <el-row :gutter="20" class="center-main">
        <el-col :span="6">
          <div class="grid-content bg-purple erwei">
            <p><img src="../assets/图标1.png" alt=""> Android版</p>
            <img src="../assets/客户端二维码.jpg" alt="" />
          </div>
        </el-col>
        <el-col :span="6">
          <div class="grid-content bg-purple erwei">
            <p><img src="../assets/图标2.png" alt=""> iPhone版</p>
            <img src="../assets/客户端二维码.jpg" alt="" />
          </div>
        </el-col>
        <el-col :span="6">
          <div class="grid-content bg-purple ttc" >
            <p class="xiazai-p"><img src="../assets/图标3.png" alt=""> Window版</p>
            <el-row>
              <el-button style="margin-left:70px" class="xiazai" type="danger" round>安装新版Window版</el-button>
            </el-row>
          </div>
        </el-col>
        <el-col :span="6">
          <div class="grid-content bg-purple ttc">
            <p class="xiazai-p"><img src="../assets/图标4.png" alt=""> Mac版</p>
            <el-row>
              <el-button style="margin-left:50px" class="xiazai" type="danger" round>安装新版Mac版</el-button>
            </el-row>
          </div>
        </el-col>
      </el-row>
      <div class="xg">
        <h3>相关直播间</h3>
        <p>你已经被我一个人包围了</p>
      </div>
      <el-row :gutter="20">
        <el-col :span="6">
            <div class="grid-content bg-purple">
                <img src="../assets/女主播1.jpg" alt="" class="zhubo">
            </div>
        </el-col>
        <el-col :span="6">
            <div class="grid-content bg-purple">
                <img src="../assets/女主播2.jpg" alt="" class="zhubo">
            </div>
        </el-col>
        <el-col :span="6">
            <div class="grid-content bg-purple">
                <img src="../assets/女主播3.jpg" alt="" class="zhubo">
            </div>
        </el-col>
        <el-col :span="6">
            <div class="grid-content bg-purple">
                <img src="../assets/女主播4.jpg" alt="" class="zhubo">
            </div>
        </el-col>
      </el-row>
    </div>
  </div>
</template>
<script>
export default {
  name: "Client",
};
</script>
<style scoped>
.client-box {
  width: 100vw;
  height: 745px;
  margin-bottom: 30px;
}
.client-box-center {
  padding-top: 55px;
}
.center-qqh2 {
  width: 100%;
  height: 81px;
  display: flex;
  font-size: 24px;
}
.center-qqh2>p{
    margin: 0;
}
.xiazai{
    margin-top: 100px;
}
.erwei>p{
    display: flex;
    align-items: center;
    float: left;
    margin-left: 40px;
}
.xiazai-p{
    display: flex;
    margin-left: 100px;
}
.xg {
  display: flex;
  height: 37px;
  margin-top: 50px;
}
.xg > h3 {
  font-size: 28px;
  display: inline-block;
  margin-left: 0;
  margin-top: 0;
}
.xg > p {
  margin-left: 20px;
  font-size: 16px;
  display: inline-block;
  margin-top: 0;
  color:rgb(218, 211, 211);
}

.zhubo{
    width: 285px;
    height: 180px;
    margin-top: 10px;
}
.ttc img{
  height: 37px;
  width: 37px;
}
</style>