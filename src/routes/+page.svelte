<script lang="ts">
	// Components
	import Summary from "$lib/components/layout/Summary.svelte";
	import Features from "$lib/components/layout/Features.svelte";
	import Testimonials from "$lib/components/layout/Testimonials.svelte";
	import CallToAction from "$lib/components/layout/CallToAction.svelte";
	import AboutTeaser from "$lib/components/layout/AboutTeaser.svelte";
	import LogoScroller from "$lib/components/layout/LogoScroller.svelte";
	import Hero from "$lib/components/layout/hero-sections/Hero.svelte";
	import UseCases from "$lib/components/layout/UseCases.svelte";
</script>

<Hero
	title="Your website. Done in minutes."
	subtitle="Skip the complexity. Skip the headaches. Just share what matters."
	imageSrc="/generated/image-a-group-of-diverse-small-business-owners.webp"
	centered={false}
/>
<LogoScroller 
	label="Join thousands who chose simple over complicated"
	logoUrls={[
		'https://logo.clearbit.com/etsy.com',
		'https://logo.clearbit.com/fiverr.com',
		'https://logo.clearbit.com/upwork.com',
		'https://logo.clearbit.com/squarespace.com'
	]}
/>

<Summary
	title="Why we exist"
	text="Building a website shouldn't feel like rocket science. We believe everyone deserves a beautiful online presence without the technical maze. While others pile on features, we focus on what actually matters: getting you online quickly, affordably, and stress-free."
/>

<Testimonials
	testimonials={[
		{
			name: "Ella Lagrange",
			position: "Illustrator",
			company: "",
			quote:
				"Built my entire portfolio during lunch. Seriously. What used to take me weeks of fighting with WordPress happened in 30 minutes. Now I actually have time for client work instead of website maintenance.",
			image:
				"/generated/image-a-professional-female-illustrator-in-her.webp"
		},
		{
			name: "Noah Bhatt",
			position: "Consultant",
			company: "",
			quote:
				"No servers to crash. No plugins to break. No security nightmares. I just write and publish. My site works perfectly, and I sleep like a baby.",
			image:
				"/generated/image-a-professional-male-business-consultant-.webp"
		},
		{
			name: "Talia Mendez",
			position: "Founder",
			company: "Talia Coaching",
			quote:
				"One link does everything. My clients get my story, services, and contact info instantly. Saved me three grand on a developer and I can update it myself in seconds.",
			image:
				"/generated/image-a-professional-female-business-coach-in-.webp"
		}
	]}
/>

<Features
	title="Built for real people"
	subtitle="No tech degree required"
	features={[
		{
			title: "Zero coding",
			description:
				"Write, click, publish. That's it. No mysterious code or confusing settings. Just focus on your message."
		},
		{
			title: "Minutes, not months",
			description:
				"Your website goes live today. Pick a design, add your words, and you're done. No waiting around."
		},
		{
			title: "Looks great everywhere",
			description:
				"Phone, tablet, laptop—your site adapts automatically. One less thing to worry about."
		},
		{
			title: "Honest pricing",
			description:
				"No hidden fees or surprise charges. Pay once, get everything. Professional results without the professional price tag."
		},
		{
			title: "Nothing to install",
			description:
				"No servers to manage or software to update. We handle the technical stuff so you don't have to."
		},
		{
			title: "Real human help",
			description:
				"Stuck? Confused? Just ask. Our support team actually wants to help, not hide behind chatbots."
		}
	]}
/>

<UseCases
	title="Perfect for"
	subtitle="Anyone who needs to be found online"
	useCases={[
		{
			title: "Freelancers who need clients",
			description: "Show off your best work without the tech headaches. Upload your portfolio, tell your story, and start getting discovered.",
			image: "/generated/image-a-small-business-owner-a-middle-aged-wom.webp",
			link: {
				href: "/use-cases/freelancer-portfolio",
				label: "See how"
			}
		},
		{
			title: "Artists ready to sell",
			description: "Turn your creativity into a stunning online gallery. No coding required—just pure focus on what you do best.",
			image: "/generated/image-an-artist-a-young-man-with-long-hair-is-.webp",
			link: {
				href: "/use-cases/artist-gallery",
				label: "See how"
			}
		},
		{
			title: "Startups moving fast",
			description: "Launch your online presence today, not next quarter. Clean, professional, and ready to grow with your business.",
			image: "/generated/image-a-startup-founder-a-young-woman-in-her-l.webp",
			link: {
				href: "/use-cases/startup-launch",
				label: "See how"
			}
		}
	]}
/>

<AboutTeaser />
<CallToAction />
