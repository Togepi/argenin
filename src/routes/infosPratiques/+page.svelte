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

<main
	style="background-image: url('/img/infosPratique.webp')"
	class=" min-h-screen bg-cover bg-center py-52 text-white"
>
	<h1 class="font-header text-center text-9xl 2xl:text-[14em]">Infos Pratiques</h1>
	<div class="mx-auto max-w-6xl bg-black py-24">
		<div class="prose prose-lg mx-auto">
			<h3>Tarif :</h3>
			<p>
				Le Gn est en prix libre. Le prix conseillé pour une PJ est de 90 chf et pour une PNJ de 30
				chf. Votre inscription ne se confirme qu’une fois le paiement effectué. Le paiement se fait
				par virement bancaire sur le site internet.
			</p>
			<p>
				Afin de pouvoir comprendre le prix conseillé, vous pouvez trouvez ici un récap' du budget de
				l'évènement: <a class="text-orange-600 underline hover:text-orange-500" href="/"
					>Budget Argenin 2025</a
				>
			</p>
			<h3>Date :</h3>
			<p>
				Le temps de jeu commence dès 22h le vendredi 5 septembre 2025 et se termine à environ 2h
				dans la nuit du samedi au dimanche. Vous pouvez arriver dès 18h le vendredi. Merci de
				quitter les lieux au cours de l’après midi du dimanche 7 septembre.
			</p>
			<h3>Lieu et Accès</h3>
			<p>
				<strong>Lieu du GN :</strong> FONDATION DES TERRAINS ET DE LA MAISON SCOUTS Centre Scout des
				Pérouses Route d’Aire-la-Ville 153 1242 Satigny / GE Suisse Carte intégré google maps
			</p>
			<p>
				<strong>En bus :</strong>
				À 20 min à pied de la gare de Saint-Cergue (nous pouvons organiser des navettes pour venir vous
				chercher).
			</p>
			<p>
				<strong>En voiture : </strong>
				Le Parking : Il y a un petit parking devant le domaine. Il y a un grand parking à 10min à pied
				[46°27'01.5"N 6°10'02.4"E]
			</p>

			<h3>Manger</h3>
			<p>
				Les repas sont fournis pour toute.x.s participantes du vendredi soir au dimanche matin.
				Merci de signaler au plus vite toute particularité alimentaire. Elle sera entièrement prise
				en compte. Fruits et breuvages disponibles tout le WE.
			</p>
			<h4>Alcool :</h4>
			<p>
				L’alcool est toléré mais non fourni. Pour des raisons d’éthiques, ne souhaitons pas
				encourager la consommation d’alcool.
			</p>
			<h3>Dormir</h3>
			<p>
				Dormir : Vous serez logés dans des dortoirs commun. Il faudra prendre un sac de couchage,
				des draps et un coussin. Les chaussures sont interdites en intérieur. Le jeu s’arrête
				pendant la nuit. Possibilité de camping pour les âmes aventureuses.
			</p>
		</div>
	</div>
</main>
