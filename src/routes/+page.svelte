<script lang="ts">
	import DuLongZu from '$lib/images/DuLongZu.png';
	import manzu from '$lib/images/manzu.png';
	import shuizu from '$lib/images/shuizu.png';
	import deangzu from '$lib/images/deangzu.png';
	import jinuozu from '$lib/images/jinuozu.png';
	import nuzu from '$lib/images/nuzu.png';
	import mengguzu from '$lib/images/mengguzu.png';
	import pumizun from '$lib/images/pumizu.png';
	import achangzu from '$lib/images/achangzu.png';
	import buyizu from '$lib/images/buyizu.png';
	import bulangzu from '$lib/images/bulangzu.png';
	import zangzu from '$lib/images/zangzu.png';
	import jingpozu from '$lib/images/jingpozu.png';
	import yaozu from '$lib/images/yaozu.png';
	import naxizu from '$lib/images/naxizu.png';
	import wazu from '$lib/images/wazu.png';
	import lahuzu from '$lib/images/lahuzu.png';
	import lisuzu from '$lib/images/lisuzu.png';
	import huizu from '$lib/images/huizu.png';
	import miaozu from '$lib/images/miaozu.png';
	import daizu from '$lib/images/daizu.png';
	import zhuangzu from '$lib/images/zhuangzu.png';
	import hanizu from '$lib/images/hanizu.png';
	import baizu from '$lib/images/baizu.png';
	import yizu from '$lib/images/yizu.png';
	import hanzu from '$lib/images/hanzu.png';

	const images = [
      { name: '独龙族', path: DuLongZu },
      { name: '满族', path: manzu },
      { name: '水族', path: shuizu },
      { name: '德昂族', path: deangzu },
      { name: '基诺族', path: jinuozu },
      { name: '怒族', path: nuzu },
      { name: '蒙古族', path: mengguzu },
      { name: '普米族', path: pumizun },
      { name: '阿昌族', path: achangzu },
      { name: '布依族', path: buyizu },
      { name: '布朗族', path: bulangzu },
      { name: '藏族', path: zangzu },
      { name: '景颇族', path: jingpozu },
      { name: '瑶族', path: yaozu },
      { name: '纳西族', path: naxizu },
      { name: '佤族', path: wazu },
      { name: '拉祜族', path: lahuzu },
      { name: '傈僳族', path: lisuzu },
      { name: '回族', path: huizu },
      { name: '苗族', path: miaozu },
      { name: '傣族', path: daizu },
      { name: '壮族', path: zhuangzu },
      { name: '哈尼族', path: hanizu },
      { name: '白族', path: baizu },
      { name: '彝族', path: yizu },
    //   { name: '汉族', path: hanzu },
   ];

   let selectedImage = images[0].path;

   function selectImage(imagePath: string) {
      selectedImage = imagePath;
   }

   $:{selectedImage}
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<h3 class="mb-8 flex items-center w-full">
	<p>Yunnan has 25 ethnic minority groups, the following is a list and sample picture of their clothing or culture. Hope you enjoy it.</p>
</h3>

<div class="button-group">
	{#each images as { name, path }}
	   <button 
	   class="px-4 py-2 mr-2 mb-2 bg-blue-400 text-white font-semibold rounded-lg shadow-md hover:bg-blue-700 focus:outline-none focus:bg-green-400 focus:ring-2 focus:ring-green-400 focus:ring-opacity-75"

	   on:click={() => selectImage(path)}>{name}</button>
	{/each}
 </div>

 <div><img src={selectedImage} alt="" /></div>



<style>
	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		flex: 0.6;
	}

	h1 {
		width: 100%;
	}

	.welcome {
		display: block;
		position: relative;
		width: 100%;
		height: 0;
		padding: 0 0 calc(100% * 495 / 2048) 0;
	}

	.welcome img {
		position: absolute;
		width: 100%;
		height: 100%;
		top: 0;
		display: block;
	}
</style>
