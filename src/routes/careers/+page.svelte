<script lang="ts">
	// Types

	// Components
	import SectionHeader from "$lib/components/layout/SectionHeader.svelte";
	import Culture from "$lib/components/layout/Culture.svelte";
	import Testimonials from "$lib/components/layout/Testimonials.svelte";
	import SecondaryHero from "$lib/components/layout/hero-sections/SecondaryHero.svelte";
	import Card from "$lib/components/ui/Card.svelte";
	import JobList, { type JobOpening } from "./JobList.svelte";

	// Icons
	import IconBriefcase from "$lib/components/icons/IconBriefcase.svelte";
	import IconUsers from "$lib/components/icons/IconUsers.svelte";
	import IconHeart from "$lib/components/icons/IconHeart.svelte";
	import IconGlobe from "$lib/components/icons/IconGlobe.svelte";

	// Constants
	const SECTION_BASE_CLASSES = "section-py section-px container mx-auto";
	const GRADIENT_BG_CLASSES =
		"bg-gradient-to-br from-gray-50 to-gray-100 dark:from-gray-900 dark:to-gray-800";
	const ICON_CONTAINER_CLASSES =
		"bg-primary-50 text-primary-600 dark:bg-primary-950 dark:text-primary-400 flex items-center justify-center rounded-full";

	const benefits = [
		{
			title: "Impact at Scale",
			description: "Help millions of non-technical users get online with beautiful, simple websites.",
			icon: IconGlobe
		},
		{
			title: "Simplicity-First Culture",
			description: "Work in an environment that values clarity, accessibility, and user-friendly design.",
			icon: IconHeart
		},
		{
			title: "Remote-First Flexibility",
			description: "Flexible work arrangements with comprehensive benefits and growth opportunities.",
			icon: IconBriefcase
		}
	];

	const openings: JobOpening[] = [
		// Engineering
		{
			title: "Senior Frontend Developer",
			department: "Engineering",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Backend Engineer",
			department: "Engineering",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Design Engineer",
			department: "Engineering",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},

		// Design
		{
			title: "UX/UI Designer",
			department: "Design",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Product Designer",
			department: "Design",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},

		// Product
		{
			title: "Product Manager",
			department: "Product",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Product Analyst",
			department: "Product",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},

		// Marketing
		{
			title: "Marketing Specialist",
			department: "Marketing",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Content Strategist",
			department: "Marketing",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Social Media Manager",
			department: "Marketing",
			location: "Remote",
			type: "Full-time",
			url: "#"
		}
	];

	const employeeTestimonials = [
		{
			name: "Elira Voss",
			position: "Front-end Developer",
			company: "Product Team",
			quote:
				"Working here has helped me grow fast—both in ownership and creativity. I shipped my own feature in week two.",
			image:
				"/generated/image-a-confident-asian-woman-in-a-modern-offi.webp"
		},
		{
			name: "Mateo Griggs",
			position: "Content Designer",
			company: "UX Team",
			quote:
				"We're small, intentional, and focused. That means your work matters every day. It's exciting to build something this useful from the ground up.",
			image:
				"/generated/image-a-friendly-hispanic-man-in-a-casual-offi.webp"
		},
		{
			name: "Azra Juno",
			position: "Engineer",
			company: "Core Platform",
			quote:
				"I came from big tech and joined to finally work on something clear and human. We build for people—not power users, not marketers—just people.",
			image:
				"/generated/image-a-warm-and-approachable-black-woman-in-a.webp"
		}
	];

	const processSteps = [
		{
			step: 1,
			title: "Simple Application",
			description:
				"Submit your application with your resume. No complex forms or lengthy requirements."
		},
		{
			step: 2,
			title: "Friendly Conversation",
			description: "Have a relaxed chat with our team about your experience and how you can help make the web simpler."
		},
		{
			step: 3,
			title: "Start Building",
			description: "Join our mission to make website creation accessible to everyone, everywhere."
		}
	];

	const values = [
		{
			icon: IconHeart,
			title: "Simplicity First",
			description: "We believe the best solutions are simple, accessible, and user-friendly."
		},
		{
			icon: IconUsers,
			title: "Inclusive Design",
			description: "We create tools that work for everyone, regardless of technical expertise."
		},
		{
			icon: IconGlobe,
			title: "Democratize the Web",
			description: "Making website creation accessible to individuals, small businesses, and creators everywhere."
		}
	];
</script>

<!-- Hero Section -->

<SecondaryHero
	title="Build something simple, meaningful, and impactful"
	subtitle="Join our mission to make website creation accessible for everyone. We're a team that believes in simplicity, empathy, and empowering non-technical users to succeed online."
	imageSrc="/generated/image-a-diverse-team-of-professionals-working-.webp"
/>

<!-- Why Join Us Section -->
<section class={SECTION_BASE_CLASSES}>
	<SectionHeader title="Why join us?" subtitle="Help us make the web simple and accessible for everyone" />

	<div class="mt-16 grid gap-4 md:grid-cols-3">
		{#each benefits as benefit}
			<Card {...benefit} />
		{/each}
	</div>
</section>

<!-- Culture Section -->
<Culture {values} />

<Testimonials testimonials={employeeTestimonials} />

<!-- Application Process -->
<section class={SECTION_BASE_CLASSES}>
	<div class="mx-auto">
		<h2 class="text-title1 mb-16">Our application process</h2>

		<div class="grid gap-12 md:grid-cols-3">
			{#each processSteps as { step, title, description }, i}
				<div class="flex flex-col">
					<div class="{ICON_CONTAINER_CLASSES} mb-6 size-11">
						<span class="text-headline">{step}</span>
					</div>
					<h3 class="text-headline mb-3">{title}</h3>
					<p class="text-body text-emphasis-low">{description}</p>
				</div>
			{/each}
		</div>
	</div>
</section>
<!-- Current Openings Section -->
<section class={GRADIENT_BG_CLASSES}>
	<div class="section-px section-py container mx-auto grid w-full items-start lg:grid-cols-2">
		<SectionHeader title="Current openings" subtitle="Find your perfect role" />

		<JobList {openings} />
	</div>
</section>
