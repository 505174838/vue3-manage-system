<template>
	<el-config-provider><!-- 自定义命名空间：使用 ElConfigProvider 包装您的根组件。(见ElementPlus) -->
		这是首页，入口页
		<router-view /><!-- 意思是，当要访问地址与路由<router-link>中的path一致时，将<router-view />替换成对应路由path对应的组件显示 -->
	</el-config-provider>
</template>

<script setup lang="ts">
	import { ElConfigProvider } from 'element-plus';
	import zhCn from 'element-plus/es/locale/lang/zh-cn';
	import { useThemeStore } from './store/theme';

	const theme = useThemeStore();
	theme.initTheme();
</script>
<style>
	@import './assets/css/main.css';
</style>
