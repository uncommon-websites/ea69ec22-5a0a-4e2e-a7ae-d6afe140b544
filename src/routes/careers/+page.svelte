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
	import IconBriefcase from "~icons/lucide/briefcase";
	import IconUsers from "~icons/lucide/users";
	import IconHeart from "~icons/lucide/heart";
	import IconGlobe from "~icons/lucide/globe";

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
			name: "Sarah Kim",
			position: "UX Designer",
			company: "Design Team",
			quote:
				"Every day I get to help make the web more accessible. Seeing small business owners launch their first website with our simple tools is incredibly rewarding.",
			image:
				"https://images.unsplash.com/photo-1534528741775-53994a69daeb?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=774&q=80"
		},
		{
			name: "David Martinez",
			position: "Frontend Developer",
			company: "Engineering Team",
			quote:
				"Our focus on simplicity challenges me to write better code. When non-technical users can easily create beautiful websites, that's when you know you've built something special.",
			image:
				"https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=774&q=80"
		},
		{
			name: "Jennifer Wu",
			position: "Customer Success Manager",
			company: "Support Team",
			quote:
				"I love helping artists, freelancers, and small businesses get online. Our simple approach means they can focus on their craft, not learning complicated tools.",
			image:
				"https://images.unsplash.com/photo-1531384441138-2736e62e0919?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=774&q=80"
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
