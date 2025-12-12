<script lang="ts">
	import FeatureBlock from './FeatureBlock.svelte';
</script>

<!-- Block 1: Text Generation for Game Dialogue -->
<FeatureBlock 
	title="Dynamic dialogue generation" 
	description="Generate contextual NPC dialogue, quest text, and narrative content that adapts to player choices in real-time."
	buttons={[
		{ text: "TRY TEXT API", icon: true },
		{ text: "VIEW DOCS" }
	]}
>
	<div class="w-full h-full bg-white border border-border rounded shadow-sm p-4 font-mono text-xs">
		<div class="flex items-center gap-2 border-b border-border pb-2 mb-4">
			<span class="text-accent">></span>
			<span class="text-muted">NPC Dialogue</span>
			<span class="w-2 h-4 bg-accent animate-pulse"></span>
		</div>
		<div class="space-y-2">
			<div class="text-[10px] text-muted mb-1">Quest Giver:</div>
			<div class="bg-primary-50 p-2 rounded text-[10px] leading-relaxed">
				"Traveler, the ancient ruins hold secrets that could save our village..."
			</div>
			<div class="h-1 bg-gray-100 w-3/4 rounded opacity-30"></div>
			<div class="h-1 bg-gray-100 w-1/2 rounded opacity-30"></div>
		</div>
	</div>
</FeatureBlock>

<!-- Block 2: Audio Generation -->
<FeatureBlock 
	title="Professional audio generation" 
	description="Create voice acting, sound effects, and ambient audio with studio-quality output optimized for game engines."
	buttons={[
		{ text: "TRY AUDIO API", icon: true }
	]}
	alignRight={true}
>
	<div class="w-full max-w-md bg-white border border-border rounded shadow-sm p-6 flex flex-col gap-4">
		<div class="flex items-center gap-2 text-xs font-mono text-muted">
			<div class="w-4 h-4 border border-current rounded-sm flex items-center justify-center">
				<div class="w-2 h-2 bg-current rounded-[1px]"></div>
			</div>
			Generating audio...
		</div>
		<div class="w-full bg-gray-100 h-1.5 rounded-full overflow-hidden">
			<div class="bg-accent h-full w-2/3"></div>
		</div>
		<div class="flex gap-1 items-end justify-center h-16">
			{#each [12, 18, 8, 24, 16, 28, 20, 32, 24, 20, 28, 16, 24, 12, 20, 8, 16, 12, 8, 4] as height}
				<div class="w-1 bg-primary-400" style="height: {height}px"></div>
			{/each}
		</div>
		<div class="mt-2 flex items-center gap-2 text-[10px] text-muted font-mono uppercase">
			<span class="w-3 h-3 border border-current rounded-full flex items-center justify-center">♪</span>
			RENDERING WAVEFORM
		</div>
	</div>
</FeatureBlock>

<!-- Block 3: Video Generation for Cutscenes -->
<FeatureBlock 
	title="Cinematic video generation" 
	description="Generate cutscenes, trailers, and in-game cinematics with consistent art direction and character models."
	buttons={[
		{ text: "TRY VIDEO API", icon: true }
	]}
>
	<div class="w-full h-full bg-white border border-border rounded shadow-sm overflow-hidden font-mono text-[10px]">
		<div class="grid grid-cols-4 gap-2 p-2 border-b border-border bg-gray-50 text-muted">
			<div>FRAME</div>
			<div>SCENE</div>
			<div>STATUS</div>
			<div>QUALITY</div>
		</div>
		{#each [
			{ frame: '001-030', scene: 'Opening', status: 'Complete', quality: '4K' },
			{ frame: '031-060', scene: 'Battle', status: 'Rendering', quality: '4K' },
			{ frame: '061-090', scene: 'Dialogue', status: 'Queue', quality: '4K' },
			{ frame: '091-120', scene: 'Transition', status: 'Queue', quality: '4K' },
			{ frame: '121-150', scene: 'Finale', status: 'Queue', quality: '4K' },
			{ frame: '151-180', scene: 'Credits', status: 'Queue', quality: '4K' }
		] as row}
			<div class="grid grid-cols-4 gap-2 p-2 border-b border-border/50 items-center">
				<div class="text-muted">{row.frame}</div>
				<div class="flex items-center gap-2">
					<div class="w-3 h-3 rounded bg-purple-400/20"></div>
					<span class="text-purple-600">{row.scene}</span>
				</div>
				<div class="text-xs {row.status === 'Complete' ? 'text-green-600' : row.status === 'Rendering' ? 'text-accent' : 'text-muted'}">{row.status}</div>
				<div class="text-xs text-muted">{row.quality}</div>
			</div>
		{/each}
	</div>
</FeatureBlock>

<!-- Block 4: Real-time Multimodal Pipeline -->
<FeatureBlock 
	title="Real-time multimodal pipeline" 
	description="Stream text, audio, and video generation in parallel with low-latency inference for dynamic gameplay experiences."
	buttons={[
		{ text: "VIEW PIPELINE", icon: true }
	]}
	alignRight={true}
>
	<div class="w-full h-full bg-white border border-border rounded shadow-sm overflow-hidden font-mono text-[10px]">
		<div class="grid grid-cols-4 gap-2 p-2 border-b border-border bg-gray-50 text-muted">
			<div>MODALITY</div>
			<div>STATUS</div>
			<div>LATENCY</div>
			<div>THROUGHPUT</div>
		</div>
		{#each [
			{ type: 'Text', status: 'Streaming', latency: '45ms', throughput: '850/s' },
			{ type: 'Audio', status: 'Streaming', latency: '120ms', throughput: '240/s' },
			{ type: 'Video', status: 'Processing', latency: '380ms', throughput: '60/s' },
			{ type: 'Text', status: 'Streaming', latency: '42ms', throughput: '920/s' },
			{ type: 'Audio', status: 'Ready', latency: '115ms', throughput: '260/s' },
			{ type: 'Video', status: 'Ready', latency: '350ms', throughput: '75/s' }
		] as row}
			<div class="grid grid-cols-4 gap-2 p-2 border-b border-border/50 items-center">
				<div class="flex items-center gap-2">
					<div class="w-3 h-3 rounded-full bg-primary-400/20"></div>
					<span class="text-primary-600">{row.type}</span>
				</div>
				<div class="text-xs {row.status === 'Streaming' ? 'text-accent' : 'text-green-600'}">{row.status}</div>
				<div class="text-xs text-muted">{row.latency}</div>
				<div class="text-xs text-muted">{row.throughput}</div>
			</div>
		{/each}
	</div>
</FeatureBlock>

<!-- Block 5: Unity & Unreal Integration -->
<FeatureBlock 
	title="Native engine integration" 
	description="Drop-in plugins for Unity and Unreal Engine with full API access and asset pipeline integration."
	buttons={[
		{ text: "GET PLUGINS", icon: true }
	]}
>
	<div class="w-full h-full bg-white border border-border rounded shadow-sm p-4 flex flex-col gap-4">
		<div class="flex items-center justify-between border-b border-border pb-2">
			<div class="text-[10px] font-mono text-muted flex items-center gap-2">
				<span class="w-2 h-2 bg-green-500 rounded-full"></span>
				Engine Plugins Active
			</div>
		</div>
		
		<!-- Plugin Cards -->
		<div class="grid grid-cols-2 gap-2">
			<div class="border border-border rounded p-3 space-y-2">
				<div class="flex items-center gap-2">
					<div class="w-6 h-6 bg-black rounded flex items-center justify-center text-white text-[8px] font-bold">U</div>
					<span class="text-[10px] font-bold">Unity</span>
				</div>
				<div class="text-[8px] text-muted">v2.4.1</div>
				<div class="flex gap-1 mt-2">
					<div class="h-1 bg-primary-400 rounded flex-1"></div>
					<div class="h-1 bg-primary-400 rounded flex-1"></div>
					<div class="h-1 bg-gray-200 rounded flex-1"></div>
				</div>
			</div>
			<div class="border border-border rounded p-3 space-y-2">
				<div class="flex items-center gap-2">
					<div class="w-6 h-6 bg-black rounded flex items-center justify-center text-white text-[8px] font-bold">UE</div>
					<span class="text-[10px] font-bold">Unreal</span>
				</div>
				<div class="text-[8px] text-muted">v5.3.2</div>
				<div class="flex gap-1 mt-2">
					<div class="h-1 bg-primary-400 rounded flex-1"></div>
					<div class="h-1 bg-primary-400 rounded flex-1"></div>
					<div class="h-1 bg-primary-400 rounded flex-1"></div>
				</div>
			</div>
		</div>

		<div class="mt-auto space-y-2">
			<div class="bg-primary-50 p-2 rounded border border-primary-200 flex gap-2 items-center">
				<div class="w-4 h-4 bg-primary-400 rounded flex items-center justify-center text-white text-[8px]">✓</div>
				<div class="text-[9px] text-primary-700 font-mono">API Connected</div>
			</div>
		</div>
	</div>
</FeatureBlock>
