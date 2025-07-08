<script lang="ts">
	// Components
	import CallToAction from "$lib/components/layout/CallToAction.svelte";

	// Icons
	import StakeholderGrid from "$lib/components/layout/StakeholderGrid.svelte";
	import Story from "./Story.svelte";
	import SecondaryHero from "$lib/components/layout/hero-sections/SecondaryHero.svelte";
	import Culture from "$lib/components/layout/Culture.svelte";

	// Constants
	const values = [
		{
			title: "Simplicity",
			description: "We believe building a website should be as easy as writing an email."
		},
		{
			title: "Accessibility",
			description: "Making web presence available to everyone, regardless of technical skill level."
		},
		{
			title: "Empowerment",
			description: "Giving people the tools to share their stories without barriers or complexity."
		}
	];
</script>

<SecondaryHero
	title="Making websites accessible to everyone"
	subtitle="No technical skills required"
	imageSrc="/generated/image-a-diverse-team-of-professionals-engaged-.webp"
/>

<!-- Story Section -->
<Story
	paragraphs={[
		"It all started with a friend who ran a small ceramics studio. She needed a simple website—just a page with her work, a bit of text, and a way for people to get in touch. Helping her build it turned into an unexpected mess. Template options, layout tools, style settings, hidden menus—it was all too much. After three frustrating hours, she gave up. It wasn't just her. We started noticing how many people, especially non-technical users, struggled to get basic websites online. Most builders assumed you had the time—and patience—to learn a new tool. A lot of people just didn't.",
		"So we set out to build the opposite. We stripped everything down to what actually mattered: a blank page, some text, maybe a few images, and a publish button. No templates, no learning curve, no design fiddling. Just type and click. The idea was simple—if you could write an email, you could build a website. We wanted to make it feel less like using a tool and more like telling your story.",
		"Since then, we've seen people from all walks of life creating their own pages—freelancers, job seekers, artists, community organizers, and plenty more. It's been incredible to hear how freeing it feels for users to do it themselves, without hiring someone or getting stuck. For many of them, it's their very first time putting something online. That's what motivates us. We believe the web should be simple, and we're here to keep it that way."
	]}
/>

<!-- Our Culture Section -->
<Culture {values} />

<!-- Team and Investors sections removed - no specific team members or investors mentioned for this company -->

<!-- CTA Section -->
<CallToAction
	title="Ready to get online?"
	subtitle="Create your website in minutes"
	description="Join thousands of individuals, freelancers, and small businesses who've created their perfect website in minutes. No technical skills required—just your ideas and our simple platform."
/>
