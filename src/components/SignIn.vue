<template>
  <div class="sign">
  <img src="../assets/signin.png">
   <el-form ref="form" :model="form" label-width="80px">
  <el-form-item label="用户名">
    <el-input v-model="form.name"></el-input>
  </el-form-item>
  <el-form-item label="密码">
    <el-input v-model="form.password"></el-input>
  </el-form-item>
  <el-form-item>
    <el-button type="primary" @click="onSubmit">登录</el-button>
    <el-button>注册</el-button>
  </el-form-item>
</el-form>
  </div>
</template>
<script>
export default {
  name: 'SignIn',
  data () {
    return {
      form: {
        name: '',
        password: ''
      }
    }
  },
  methods: {
    onSubmit () {
      this.$http.post('url', this.qs.stringify({ 'bar': 123 }))
        .then(function (response) {
          console.log(response)
        })
    }
  }
}
</script>
