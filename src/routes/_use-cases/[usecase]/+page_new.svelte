<script lang="ts">
	// Types
	import type { PageData } from "./$types";

	// Components
	import Hero from "$lib/components/layout/hero-sections/Hero.svelte";
	import Summary from "$lib/components/layout/Summary.svelte";
	import Features from "$lib/components/layout/Features.svelte";
	import Testimonials from "$lib/components/layout/Testimonials.svelte";
	import CallToAction from "$lib/components/layout/CallToAction.svelte";

	// Icons
	import IconStar from "~icons/lucide/star";

	// Props
	const { data }: { data: PageData } = $props();

	// Icon mapping - use star for all icons since others don't exist
	const iconMap: Record<string, any> = {
		"users": IconStar,
		"clipboard-list": IconStar,
		"chart-bar": IconStar,
		"shield-check": IconStar,
		"chart-line": IconStar,
		"shield-alert": IconStar,
		"presentation-chart": IconStar,
		"document-check": IconStar,
		"code-bracket": IconStar,
		"cpu-chip": IconStar,
		"user-group": IconStar,
		"chart-bar-square": IconStar,
		"academic-cap": IconStar,
		"clipboard-document-check": IconStar,
		"chart-pie": IconStar,
		"cog": IconStar
	};

	// Convert string icons to components
	let processedFeatures = $derived(
		data?.features?.items?.map(feature => ({
			...feature,
			icon: iconMap[feature.icon] || IconStar
		})) || []
	);
</script>

{#if data?.hero}
	<Hero
		title={data.hero.title}
		subtitle={data.hero.subtitle}
		imageSrc={data.hero.imageSrc}
		callsToAction={data.hero.callsToAction}
	/>
{/if}

{#if data?.summary}
	<Summary title={data.summary.title} text={data.summary.text} />
{/if}

{#if data?.testimonials}
	<Testimonials testimonials={data.testimonials.map(t => ({
		name: t.author,
		position: t.role,
		company: t.role,
		quote: t.quote,
		image: t.imageSrc
	}))} />
{/if}

{#if data?.features}
	<Features
		title={data.features.title}
		subtitle={data.features.subtitle}
		features={processedFeatures}
	/>
{/if}

{#if data?.cta}
	<CallToAction
		title={data.cta.title}
		subtitle={data.cta.subtitle}
		description={data.cta.description}
		callsToAction={data.cta.callsToAction}
	/>
{/if}