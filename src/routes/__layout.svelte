<script context='module'>
import {animate} from 'motion'
import { onMount } from 'svelte';
</script>
<script>
	import '../styles/main.css'
	import '../styles/typography.css'
	onMount(async()=>{
		animate('.ctaBtn',{transform:['scale(1)','scale(1.1)']},{repeat:Infinity,direction:'alternate-reverse',duration:1})
	})
</script>
<header>
	<nav>
		<div class="logo">
			<a href="/">
			<img src="/favicon.png" alt="logo" width=40 height=40>
			</a>
		</div>
		<ul>
			<li><a href="/">Home</a> </li>
			<li><a href="/about">About</a> </li>
			<li><a href="/contact">Contact</a></li>
		</ul>
		<div class="cta"><button class="ctaBtn">Book Now</button></div>
	</nav>
</header>

<style>
	nav{
		width:100%;
		padding:0px 20px;
		height:60px;
		display:grid;
		justify-content: space-between;
		align-items: center;
		grid-template-areas:
		'logo links cta'
		'logo links cta'
		;
	}
	.logo{
		grid-area: logo;
	}
	ul{
		grid-area: links;
		list-style: none;
		display:flex;
		flex-direction: row;
		gap:10px;
	}
	.cta{
		grid-area:cta;
	}
	.ctaBtn{
		background:var(--green);
		color: var(--tan1);
		border:none;
		padding:5px 5px;
	}
</style>
<slot/>