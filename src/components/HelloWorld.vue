<template>
  <div class="wrapper">
    <div class="title">
      <el-button type="primary" @click="goBack">返回</el-button>
    </div>
    <div class="content">
      <div class="content_top">售币机模板设置</div>
      <div class="content_bottom">
        <div class="content_left"></div>

        <div class="content_right">
          <el-form ref="form" :model="form" label-width="80px">
            <el-form-item label="页面名称">
              <el-input v-model="form.name"></el-input>
            </el-form-item>
            <el-form-item label="页面标题">
              <el-input v-model="form.title"></el-input>
            </el-form-item>
            <el-form-item label="页面描述">
              <el-input v-model="form.desc"></el-input>
            </el-form-item>
            <el-form-item label="客服电话">
              <el-input v-model="form.phone"></el-input>
            </el-form-item>
            <el-form-item>
              <el-checkbox-group v-model="form.type">
                <el-checkbox label="关联游戏币满减（满送）优惠" name="type"></el-checkbox>
                <p>若勾选此选项，售币机会享受满减（满送）优惠</p>
                <el-checkbox label="开启余币自提" name="type"></el-checkbox>
                <p>若勾选此选项，用户可将微信余币通过售币机提取出来</p>
                <el-checkbox label="自定义游戏币充值数量" name="type"></el-checkbox>
                <p>勾选启用自定义购币功能，启用自定义购币不占用以下套餐数量</p>
              </el-checkbox-group>
            </el-form-item>
            <el-form-item label="充值设置">
              <p>（请设置用户充值的金额，最多可设置6项。如果是脉冲版售币机，建议单次出币不超过500币，以防出错！）</p>
              <div class="settingItem">
                <el-input></el-input>元
                <el-input></el-input>币
                <el-button>+</el-button>
                <el-button>-</el-button>
              </div>
            </el-form-item>
          </el-form>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      form: {
        name: "",
        title: "",
        desc: "",
        phone: "",
        type: []
      }
    };
  },
  methods: {
    goBack() {
      alert("返回");
    }
  }
};
</script>

<style scoped lang="scss">
.wrapper {
  background-color: grey;
  // height: 100vh;
  height: 100%;
  .title {
    margin: 20px 0;
  }
  .content {
    background-color: #fff;
    margin: 20px;
    padding:  0 0 100px 0;
    .content_top {
      padding: 20px;
      border-bottom: solid 1px #ccc;
    }
    .content_bottom {
      padding: 20px;
      display: flex;
      justify-content: center;

      .content_left {
        flex: 1;
      }

      .content_right {
        flex: 1;
      }
    }
  }
}
.settingItem{
  display: flex;
}
</style>
