<script lang="ts">
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
<article
	style="background-image: url('/img/landing_hero_bg3.webp')"
	class="bg-black bg-cover bg-center py-44 text-white"
>
	<section class="mx-auto flex max-w-7xl flex-col items-center justify-center px-5 text-center">
		<div class=" max-w-7xl">
			<img src="/img/landing_title.webp" alt="logo" class="w-full -translate-x-6" />
		</div>

		<h2 class="mt-2 max-w-xl text-xl font-bold text-white md:text-4xl">
			Argenin, un jeu de rôle grandeur nature basé sur le monde de
			<a href="https://nssn-jdr.com/" target="_blank">
				<span class="text-orange-600 hover:underline">Nihil Sub Sole Novum. </span>
			</a>
		</h2>
		<div class=" mt-4 flex items-center justify-center gap-8 text-xl">
			<p>Place disponible :</p>
			<p class=" text-xl">PJ:45</p>
			<p class=" text-xl">PNJ:12</p>
		</div>
		<section class="flex">
			<ul class="mt-2 flex gap-4 rounded py-3">
				<li>5-7 Septembre 2025</li>
				<Separator orientation="vertical" />
				<li>Centre Scout de Genève</li>
				<Separator orientation="vertical" />
				<li>Prix conseillé : 90chf</li>
			</ul>
		</section>
		<section class="mt-2 flex gap-2">
			<Button href="/auth" size="lg" class="relative">Inscription</Button>

			<Button href="/wiki" variant="ghost" size="lg">
				<span class="group flex items-center gap-2 text-lg"
					>Je débute <ArrowRight class="transition-all group-hover:ml-2" /></span
				>
			</Button>
		</section>
	</section>
</article>
<article
	style="background-image: url('/img/landing_hero_bg1.webp')"
	class="group bg-black bg-cover py-32 saturate-0 duration-500 hover:saturate-100"
>
	<div class="mx-auto max-w-7xl space-y-8 px-5 transition-all">
		<h1 class="py-12 text-center text-5xl text-white md:text-9xl">Note d'intention</h1>
		<div class="relative flex flex-col items-center">
			<a
				href="/"
				class="absolute top-[90px] left-[870px] opacity-90 transition-all duration-500 group-hover:opacity-100 focus:scale-90"
			>
				<img
					src="/img/landing_synopsis_presSyn2.webp"
					alt="Button for synopsis"
					class="transition-transform duration-500 hover:scale-90"
				/>
			</a>
			<div
				class="absolute top-[290px] left-[940px] flex opacity-0 transition-all duration-500 group-hover:opacity-100"
			>
				<img src="/img/landing_syn_pointer_invert.webp" alt="" />
				<div class="  border bg-black p-2 px-4 text-xs text-white">Tout le synopsis</div>
			</div>
			<a
				href="/"
				class="absolute top-[205px] left-[868px] opacity-90 transition-all duration-500 group-hover:opacity-100 focus:rotate-12"
			>
				<img
					src="/img/landing_synopsis_presSyn3.webp"
					alt="Button for synopsis"
					class="transition-transform duration-500 hover:rotate-12"
				/>
			</a>
			<div
				class="absolute top-[90px] left-[940px] flex opacity-0 transition-all duration-500 group-hover:opacity-100"
			>
				<img src="/img/landing_syn_pointer.webp" alt="" />
				<div class="  border bg-black p-2 px-4 text-xs text-white">Tout le synopsis</div>
			</div>

			<img src="/img/landing_synopsis.webp" alt=" la note d'intention" class="rounded-3xl" />
			<section class="mt-8 flex flex-wrap gap-2">
				<span class="text-white uppercase">Thèmes :</span>
				<Badge variant="secondary">Post-apo</Badge>
				<Badge variant="secondary">Fantaisie</Badge>
				<Badge variant="secondary">Politique</Badge>
				<Badge variant="secondary">Survie</Badge>
				<Badge variant="secondary">Guerre</Badge>
			</section>
		</div>
	</div>
</article>
<article class="bg-black bg-fixed bg-center py-32 pb-52">
	<section class="mx-auto max-w-7xl">
		<div class="prose mx-auto p-8 text-center text-white">
			<h2>Concepts clés</h2>
			<h3 class="text-nowrap">Comprendre Argenin en 6 phrases.</h3>
		</div>
		<div class=" mt-32 grid w-full lg:grid-cols-3">
			<article class="prose mx-auto p-5 text-white">
				<h3 class="text-center">guerre constante</h3>
				<img src="/img/nego.webp" alt="Deux personnes armées" class="rounded" />
				<p class="mt-8 bg-black px-5">
					Argenin est avant tout une l'histoire d'un guerre, vous allez participer à des batailles
					scénarisées.
				</p>
			</article>
			<article class="prose mx-auto p-5 text-white">
				<h3 class="text-center">Environnement hostile</h3>
				<img src="/img/laguerre.webp" alt="Deux personnes en négociation" class="rounded" />
				<p class="mt-8 bg-black px-5">
					Si les batailles captivent par leur intensité, la guerre se gagne aussi en dehors des
					champs de bataille.
				</p>
			</article>
			<article class="prose mx-auto p-5 text-white">
				<h3 class="text-center">Conséquences psychologique</h3>
				<img src="/img/sante.webp" alt="Une personne triste" class="rounded" />
				<p class="mt-8 bg-black px-5">
					Survivre en temps de guerre exige une préparation constante.
				</p>
			</article>
			<article class="prose mx-auto p-5 text-white">
				<h3 class="text-center">jeu d'équipe</h3>
				<img src="/img/sante.webp" alt="Une personne triste" class="rounded" />
				<p class="mt-8 bg-black px-5">
					Survivre en temps de guerre exige une préparation constante. Sans le matériel adéquat,
					votre personnage risque de subir des conséquences mentales graves, représentées par des
					cartes mentales.
				</p>
			</article>
			<article class="prose mx-auto p-5 text-white">
				<h3 class="text-center">jeu de diplomatie</h3>
				<img src="/img/sante.webp" alt="Une personne triste" class="rounded" />
				<p class="mt-8 bg-black px-5">
					Survivre en temps de guerre exige une préparation constante. Sans le matériel adéquat,
					votre personnage risque de subir des conséquences mentales graves, représentées par des
					cartes mentales.
				</p>
			</article>
			<article class="prose mx-auto p-5 text-white">
				<h3 class="text-center">scènes de nuit</h3>
				<img src="/img/sante.webp" alt="Une personne triste" class="rounded" />
				<p class="mt-8 bg-black px-5">
					Survivre en temps de guerre exige une préparation constante. Sans le matériel adéquat,
					votre personnage risque de subir des conséquences mentales graves, représentées par des
					cartes mentales.
				</p>
			</article>
			<Button class="mx-auto" variant="secondary" href="/wiki#la-guerre"
				>Wiki règles de la santé mentale</Button
			>
		</div>
	</section>
</article>

<div
	class="bg-black px-5 pb-32 md:pb-96 xl:px-0"
	style="background-image: url('/img/landing_actu_bg.webp')"
>
	<h2 class=" py-16 text-center text-5xl text-white md:py-40 md:text-9xl">
		Choisissez votre camps
	</h2>
	<article class="relative mx-auto grid max-w-7xl grid-cols-1 gap-10 md:h-[660px] md:grid-cols-2">
		<a
			href="/wiki"
			style="background-image: url('/img/landing_RepMarch.webp')"
			class="group relative flex flex-col items-center justify-between rounded-lg bg-cover bg-center py-12 text-white hover:brightness-110 md:py-0"
		>
			<div>
				<h3 class="font-rep pt-16 text-center text-4xl tracking-tighter">
					La République Marchande
				</h3>
				<p class="mx-auto mt-2 max-w-md bg-black text-center text-lg md:bg-transparent">
					Un état qui rêve d'incarner la renaissance de la civilisation.
				</p>
			</div>

			<div
				class="mb-4 flex items-center justify-center gap-1 rounded-lg border-t border-b border-t-white/30 border-b-black/50
				 bg-gradient-to-b from-white/10 px-8 py-1 text-center shadow backdrop-blur group-hover:to-white/20"
			>
				<p>Page Wiki de la République</p>
				<ArrowUpRight size="16" class="    stroke-white opacity-50 group-hover:opacity-100" />
			</div>
		</a>
		<img
			src="/img/vs.webp"
			alt="Versus symbole"
			class=" pointer-events-none left-1/2 z-40 mx-auto h-52 w-52 md:absolute md:top-1/2 md:-translate-1/2 2xl:h-60 2xl:w-60"
		/>
		<a
			href="wiki/"
			style="background-image: url('/img/landing_Libre.webp')"
			class="group relative flex flex-col items-center justify-between rounded-lg bg-cover bg-center py-12 text-white hover:brightness-110 md:py-0"
		>
			<div>
				<h3
					class=" font-zone text-center text-6xl tracking-tighter text-shadow-[0_0.3rem_2px_rgb(0_0_0_/_1)] md:translate-y-5 md:pt-16"
				>
					Les Zones Libres
				</h3>
				<p
					class=" mx-auto mt-2 max-w-md bg-black text-center text-lg md:translate-y-5 md:bg-transparent"
				>
					Des peuples qui refusent de se soumettre au dictat de la République.
				</p>
			</div>

			<div
				class="mb-4 flex items-center justify-center gap-1 rounded-lg border-t border-b border-t-white/30 border-b-black/50
				 bg-gradient-to-b from-white/10 px-8 py-1 text-center shadow backdrop-blur group-hover:to-white/20"
			>
				<p>Page Wiki des Zones Libres</p>
				<ArrowUpRight size="16" class="    stroke-white opacity-50 group-hover:opacity-100" />
			</div>
		</a>
	</article>
</div>
