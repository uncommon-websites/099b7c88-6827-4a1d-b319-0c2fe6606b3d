<script lang="ts">
	import { onMount } from 'svelte';
	
	let showBanner = true;
</script>

{#if showBanner}
	<div class="bg-primary-50 border-b border-border py-2 px-4 text-xs font-mono flex justify-center items-center relative">
		<div class="flex items-center gap-2">
			<span class="text-muted">Now supporting Unity and Unreal Engine integrations.</span>
			<a href="#" class="underline decoration-muted hover:text-accent transition-colors">Learn more.</a>
		</div>
		<button 
			class="absolute right-4 text-muted hover:text-foreground"
			aria-label="Close banner"
			onclick={() => showBanner = false}
		>
			<svg width="12" height="12" viewBox="0 0 12 12" fill="none" xmlns="http://www.w3.org/2000/svg">
				<path d="M9 3L3 9M3 3L9 9" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
			</svg>
		</button>
	</div>
{/if}

<nav class="border-b border-border bg-background sticky top-0 z-50">
	<div class="container-custom h-16 flex items-center justify-between">
		<!-- Logo -->
		<a href="/" class="text-xl font-bold tracking-tight flex items-center gap-2">
			<svg width="24" height="14" viewBox="0 0 116 68" fill="none" xmlns="http://www.w3.org/2000/svg" class="text-foreground">
				<path fill-rule="evenodd" clip-rule="evenodd" d="M44.6215 56.0343C46.6079 53.651 49.5502 52.2726 52.6531 52.2726H94.8018C106.35 52.2726 115.711 42.9114 115.711 31.3637V20.909C115.711 9.36134 106.35 0 94.8018 0H86.6303C83.5277 0 80.5851 1.37818 78.599 3.76179L71.8003 11.9201C69.814 14.3037 66.8716 15.6818 63.7688 15.6818H21.62C10.0722 15.6818 0.710938 25.043 0.710938 36.5909V47.0454C0.710938 58.5933 10.0722 67.9546 21.62 67.9546H29.7916C32.8942 67.9546 35.8367 66.5765 37.8229 64.1929L44.6215 56.0343ZM100.029 20.909C100.029 18.022 97.6888 15.6818 94.8018 15.6818H78.7895C75.6866 15.6818 72.7443 17.0599 70.7579 19.4435L63.9593 27.602C61.9731 29.9854 59.0306 31.3637 55.9279 31.3637H21.62C18.7331 31.3637 16.3927 33.704 16.3927 36.5909V47.0454C16.3927 49.9324 18.7331 52.2726 21.62 52.2726H37.6324C40.7352 52.2726 43.6776 50.8945 45.664 48.5109L52.4626 40.3526C54.4488 37.969 57.3913 36.5909 60.4939 36.5909H94.8018C97.6888 36.5909 100.029 34.2507 100.029 31.3637V20.909Z" fill="currentColor"/>
			</svg>
			<span class="font-sans font-semibold">Core Flow</span>
		</a>

		<!-- Links -->
		<div class="hidden md:flex items-center gap-8 font-mono text-xs text-muted">
			<a href="#" class="hover:text-foreground transition-colors">Platform</a>
			<a href="#" class="hover:text-foreground transition-colors">Models</a>
			<a href="#" class="hover:text-foreground transition-colors">Pricing</a>
			<a href="#" class="hover:text-foreground transition-colors">Blog</a>
			<a href="#" class="hover:text-foreground transition-colors">Docs</a>
		</div>

		<!-- CTA -->
		<div class="flex items-center gap-4">
			<a href="#" class="hidden md:flex items-center gap-2 border border-border px-3 py-1.5 text-xs font-mono hover:bg-primary-50 transition-colors uppercase">
				Get Started
				<svg width="12" height="12" viewBox="0 0 12 12" fill="none" xmlns="http://www.w3.org/2000/svg">
					<path d="M1 11L11 1M11 1H3M11 1V9" stroke="currentColor" stroke-width="1.5"/>
				</svg>
			</a>
			<div class="md:hidden">
				<!-- Mobile Menu Icon -->
				<svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
					<line x1="3" y1="12" x2="21" y2="12"></line>
					<line x1="3" y1="6" x2="21" y2="6"></line>
					<line x1="3" y1="18" x2="21" y2="18"></line>
				</svg>
			</div>
		</div>
	</div>
</nav>
