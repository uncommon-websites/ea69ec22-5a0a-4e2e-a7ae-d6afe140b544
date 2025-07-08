<script lang="ts">
	// Types
	import type { PageProps } from "./$types";

	// Components
	import Features from "$lib/components/layout/Features.svelte";
	import Testimonials from "$lib/components/layout/Testimonials.svelte";
	import CallToAction from "$lib/components/layout/CallToAction.svelte";
	import Pricing from "$lib/components/layout/Pricing.svelte";

	// Props
	const { data }: PageProps = $props();
</script>

<Pricing />

<Testimonials
	testimonials={[
		{
			name: "Allie Rutherford",
			position: "Illustrator",
			company: "Freelance Artist",
			quote:
				"I launched my website in under 10 minutes. It felt like writing an email — that's it. No technical knowledge needed, and it looks professional.",
			image:
				"/generated/image-a-professional-headshot-of-a-young-woman.webp"
		},
		{
			name: "Malik Tan",
			position: "Founder",
			company: "Monsoon Studio",
			quote:
				"We needed something fast and simple. This platform let us skip the tech headaches entirely. Best ROI we've seen — saved us thousands on web development.",
			image:
				"/generated/image-a-professional-headshot-of-a-middle-aged.webp"
		},
		{
			name: "Eric Lau",
			position: "Product Designer",
			company: "Tech Startup",
			quote:
				"My parents used it. They don't even use smartphones. That's how simple it is. If they can build a website, anyone can.",
			image:
				"/generated/image-a-professional-headshot-of-a-young-asian.webp"
		}
	]}
/>

<CallToAction
	title="Don't overthink it"
	subtitle="Start now. No account needed."
	description="Take 5 minutes. Create something real. Share it with the world. No credit card. No learning curve. Just your site—live in minutes."
	imageSrc="/generated/image-a-cheerful-small-business-owner-sitting-.webp"
	callsToAction={[
		{
			href: "/get-started",
			label: "Make your site now",
			variant: "primary"
		},
		{
			href: "/contact",
			label: "Have questions?",
			variant: "secondary"
		}
	]}
/>
