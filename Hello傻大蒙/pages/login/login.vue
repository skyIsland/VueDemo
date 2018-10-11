<template>
	<form class='loginView' @submit="login">
		<view class="input-view">
			<view class="label-view">
				<text class="label">账号 </text>
			</view>
			<input class="input" type="text" placeholder="请输入用户名" name="nameValue" value="admin"/>
		</view>
		<view class="input-view">
			<view class="label-view">
				<text class="label">密码</text>
			</view>
			<input class="input" type="password" placeholder="请输入密码" name="passwordValue" />
		</view>
		<view class="button-view">
			<button type="default" class="login" hover-class="hover" formType="submit">登录</button>
			<button type="default" class="register" hover-class="hover" @click="register">免费注册</button>
		</view>
	</form>
</template>

<script>
	export default {
		data: {

		},
		methods: {
			login(e) {
				console.log("得到账号:" + e.detail.value.nameValue + ';得到密码:' + e.detail.value.passwordValue)
				uni.request({
					url: 'http://139.199.207.128:4399/Api/User/Login',
					method:'POST',
					header:{
						'content-type':'application/x-www-form-urlencoded'
					},
					data: {
						name: e.detail.value.nameValue,
						password: e.detail.value.passwordValue
					},
					success: (data) => {
						console.log(JSON.stringify(data));
						var ret = data.data;
						uni.showToast({
							title: ret.Message,
							duration: 2000,
							success:function(){
								if (ret.Result) {
									uni.setStorage({
										key: 'IsSigned',
										data: 'true'
									});
									uni.setStorage({
										key: 'UserName',
										data: e.detail.value.nameValue
									});
									uni.redirectTo({
										url: '../center/center'
									});
								}
							}
						});
					}
				});
			},
			register() {
				uni.showToast({
					title: '攻城狮开发中...',
					duration: 2000
				});
			}
		}
	}
</script>

<style>

</style>
