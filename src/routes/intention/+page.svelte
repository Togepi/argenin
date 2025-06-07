<script lang="ts">
	import { dictionary } from './../../../.svelte-kit/generated/client-optimized/app.js';
	import type { PageProps } from './$types';
	import { enhance } from '$app/forms';
	import { Button } from '$lib/components/ui/button';
	import { Badge } from '$lib/components/ui/badge';
	import { Separator } from '$lib/components/ui/separator';
	import MainNav from '$lib/components/navigation/MainNav.svelte';
	import { ArrowRight, ArrowUpRight, BookOpen } from '@lucide/svelte';

	let { data }: PageProps = $props();

	let name = $state('');
	let message = $state('');
	let characterCount = $derived(message.length);
</script>

<MainNav />

<main
	style="background-image: url('/img/infosPratique.webp')"
	class=" min-h-screen bg-cover bg-center py-52 text-white"
>
	<h1 class="font-header text-center text-4xl md:text-9xl 2xl:text-[14em]">Note d'intention</h1>
	<div>
		<div class="prose prose-lg mx-auto mt-32">
			<h2>Pitch</h2>
			<h3>Argenin chapitre 1 : Les braises de la rébellion</h3>
			<p>
				Alb Perion est mort, et avec lui la fragile paix qu'il maintenait. Alors que vous vous
				rendez à son enterrement, les factions se préparent : certaines veulent éviter le chaos,
				d'autres y voient une chance de s'enrichir ou de prendre le pouvoir. La guerre froide
				pourrait bien devenir brûlante…
			</p>
			<h4>Thèmes :</h4>
			<ul class="flex flex-wrap gap-2 *:rounded-lg *:bg-neutral-950 *:p-2 *:px-3">
				<li>Post-apo</li>
				<li>fantaisie</li>
				<li>guerre-froide</li>
				<li>politique</li>
				<li>combats</li>
				<li>survie</li>
			</ul>
			<h2>Introduction</h2>
			<p>
				Pendant près d’un demi-siècle, le Petit Monde fut silencieux. La guerre s’était arrêtée
				brutalement et les survivantes rampaient lentement hors des décombres de l’Ancien Monde.
				Alors que le Petite Peuple allait reprendre ses droits sur la terre, il fut surprit de
				constater l’apparition soudaine de larges étendues de forêts dans tout le Petit Monde. La
				magie reprenait sa place et le Petit Peuple n’en ferait pas partie. Certaines essayèrent de
				se reconnecter avec le monde mystique pour en tirer les pouvoirs surnaturels qui avaient
				fait la force de leurs ancêtres mais sans succès.
			</p>
		</div>
	</div>
</main>
