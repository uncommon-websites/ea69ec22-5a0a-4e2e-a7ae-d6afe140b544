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
	title="Build a website in minutes"
	subtitle="No code. No clutter. Just your content."
	imageSrc="/generated/image-a-group-of-diverse-small-business-owners.webp"
	centered={false}
/>
<LogoScroller 
	label="Trusted by creative professionals and small businesses"
	logoUrls={[
		'https://logo.clearbit.com/etsy.com',
		'https://logo.clearbit.com/fiverr.com',
		'https://logo.clearbit.com/upwork.com',
		'https://logo.clearbit.com/squarespace.com'
	]}
/>

<Summary
	title="What we do"
	text="We provide a service for individuals and businesses to create super simple websites, focusing on ease of use and accessibility for non-technical users. Our platform prioritizes simplicity, speed, and affordability over highly customized or complex web functionalities."
/>

<Testimonials
	testimonials={[
		{
			name: "Ella Lagrange",
			position: "Illustrator",
			company: "",
			quote:
				"I made my portfolio in a lunch break. What would have taken me weeks of wrestling with templates happened in 30 minutes. I saved so much time I could focus on actual client work.",
			image:
				"/generated/image-a-professional-female-illustrator-in-her.webp"
		},
		{
			name: "Noah Bhatt",
			position: "Consultant",
			company: "",
			quote:
				"Nothing to set up. Just pure writing. I eliminated all the technical risks of managing hosting, security, and updates. My site just works, and I sleep better at night.",
			image:
				"/generated/image-a-professional-male-business-consultant-.webp"
		},
		{
			name: "Talia Mendez",
			position: "Founder",
			company: "Talia Coaching",
			quote:
				"I send people one link and they get all they need. This saved me $3000 compared to hiring a developer, and I can update it myself whenever I want.",
			image:
				"/generated/image-a-professional-female-business-coach-in-.webp"
		}
	]}
/>

<Features
	title="Why choose us"
	subtitle="Everything you need to get online quickly"
	features={[
		{
			title: "No code required",
			description:
				"Create your website without writing a single line of code. Our intuitive interface makes web building accessible to everyone."
		},
		{
			title: "Lightning fast setup",
			description:
				"Get your website live in minutes, not hours. Choose a template, add your content, and you're ready to go."
		},
		{
			title: "Mobile responsive",
			description:
				"Your website automatically looks perfect on all devices. No need to worry about technical details or complex configurations."
		},
		{
			title: "Affordable pricing",
			description:
				"Professional websites shouldn't break the bank. Our simple pricing makes it easy for anyone to afford a quality online presence."
		},
		{
			title: "Built-in hosting",
			description:
				"Everything you need is included in one place. No separate hosting accounts or technical setup required."
		},
		{
			title: "24/7 support",
			description:
				"Get help whenever you need it with our friendly support team. We're here to make your website journey smooth and stress-free."
		}
	]}
/>

<UseCases
	title="Use Cases"
	subtitle="Real-world applications for your simple website needs"
	useCases={[
		{
			title: "Freelancers showcase their work",
			description: "Create a professional portfolio in minutes to attract clients. No technical skills needed - just upload your work and share your story.",
			image: "/generated/image-a-small-business-owner-a-middle-aged-wom.webp",
			link: {
				href: "/use-cases/freelancer-portfolio",
				label: "Learn more"
			}
		},
		{
			title: "Artists display their creations",
			description: "Transform your art into an online gallery that showcases your unique style. Perfect for painters, photographers, and creative professionals.",
			image: "/generated/image-an-artist-a-young-man-with-long-hair-is-.webp",
			link: {
				href: "/use-cases/artist-gallery",
				label: "Learn more"
			}
		},
		{
			title: "Startups launch their presence",
			description: "Get your business online quickly with a clean, professional website. Focus on your product while we handle the technical details.",
			image: "/generated/image-a-startup-founder-a-young-woman-in-her-l.webp",
			link: {
				href: "/use-cases/startup-launch",
				label: "Learn more"
			}
		}
	]}
/>

<AboutTeaser />
<CallToAction />
