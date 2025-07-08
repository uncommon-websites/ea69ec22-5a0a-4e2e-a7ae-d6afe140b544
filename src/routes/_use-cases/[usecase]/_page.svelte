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
	import IconUsers from "~icons/lucide/users";
	import IconClipboardList from "~icons/lucide/clipboard-list";
	import IconBarChart from "~icons/lucide/bar-chart";
	import IconShieldCheck from "~icons/lucide/shield-check";
	import IconTrendingUp from "~icons/lucide/trending-up";
	import IconShieldAlert from "~icons/lucide/shield-alert";
	import IconPresentationChart from "~icons/lucide/presentation-chart-line";
	import IconDocumentCheck from "~icons/lucide/document-check";
	import IconCode from "~icons/lucide/code";
	import IconCpu from "~icons/lucide/cpu";
	import IconUserGroup from "~icons/lucide/users";
	import IconBarChart3 from "~icons/lucide/bar-chart-3";
	import IconGraduationCap from "~icons/lucide/graduation-cap";
	import IconClipboardCheck from "~icons/lucide/clipboard-check";
	import IconPieChart from "~icons/lucide/pie-chart";
	import IconSettings from "~icons/lucide/settings";

	// Props
	const { data }: { data: PageData } = $props();

	// Icon mapping
	const iconMap: Record<string, any> = {
		"users": IconUsers,
		"clipboard-list": IconClipboardList,
		"chart-bar": IconBarChart,
		"shield-check": IconShieldCheck,
		"chart-line": IconTrendingUp,
		"shield-alert": IconShieldAlert,
		"presentation-chart": IconPresentationChart,
		"document-check": IconDocumentCheck,
		"code-bracket": IconCode,
		"cpu-chip": IconCpu,
		"user-group": IconUserGroup,
		"chart-bar-square": IconBarChart3,
		"academic-cap": IconGraduationCap,
		"clipboard-document-check": IconClipboardCheck,
		"chart-pie": IconPieChart,
		"cog": IconSettings
	};

	// Convert string icons to components
	let processedFeatures = $derived(
		data?.features?.items?.map(feature => ({
			...feature,
			icon: iconMap[feature.icon] || IconUsers
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
	<Testimonials testimonials={data.testimonials} />
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
