<section class="py-20 border-b border-border">
	<div class="container-custom">
		<div class="grid grid-cols-1 md:grid-cols-2 gap-16">
			
			<!-- Left Column: CTA & Visual -->
			<div class="flex flex-col h-full">
				<div class="mb-8">
					<p class="font-mono text-xs text-muted mb-4">Start building</p>
					<h2 class="text-2xl font-medium mb-4">Transform your game development pipeline</h2>
					<p class="text-muted font-light mb-8 text-sm leading-relaxed max-w-md">
						Core Flow provides frontier AI models for scalable content generation, enabling studios to create more with less infrastructure overhead
					</p>
					<div class="flex gap-3 mb-12">
						<button class="border border-border px-3 py-1.5 text-xs font-mono uppercase hover:bg-primary-50 transition-colors flex items-center gap-2">
							GET API ACCESS
							<span class="text-muted border border-muted/30 rounded px-1 text-[9px] min-w-[16px] text-center">A</span>
						</button>
						<button class="border border-border px-3 py-1.5 text-xs font-mono uppercase hover:bg-primary-50 transition-colors flex items-center gap-2">
							VIEW DOCS
							<span class="text-muted border border-muted/30 rounded px-1 text-[9px] min-w-[16px] text-center">D</span>
						</button>
					</div>
				</div>
				
				<!-- Abstract Visual -->
				<div class="mt-auto w-full h-48 bg-gradient-to-br from-gray-900 to-black relative overflow-hidden flex items-center justify-center">
					<!-- Flowing lines representing content generation -->
					{#each Array(60) as _, i}
						<div 
							class="h-0.5 bg-primary-400/30 absolute" 
							style="
								left: 0;
								right: 0;
								top: {(i / 60) * 100}%;
								opacity: {Math.random() * 0.5 + 0.2};
								transform: translateX({Math.sin(i) * 20}px);
							"
						></div>
					{/each}
					<div class="absolute inset-0 flex items-center justify-center">
						<div class="bg-black/80 text-white font-mono text-[10px] px-3 py-1.5 z-10 border border-primary-500/30">
							CORE FLOW
						</div>
					</div>
				</div>
			</div>

			<!-- Right Column: Updates -->
			<div>
				<p class="font-mono text-xs text-muted mb-8">Latest updates</p>
				
				<div class="space-y-12">
					<!-- Update 1 -->
					<div class="flex gap-8 group">
						<div class="font-mono text-xs text-muted w-24 shrink-0 pt-1">January 15</div>
						<div>
							<h3 class="font-medium text-sm mb-2 group-hover:text-accent transition-colors cursor-pointer">Unreal Engine 5.4 Plugin Released</h3>
							<p class="text-xs text-muted leading-relaxed mb-3">
								Our new Unreal Engine plugin brings Core Flow's multimodal generation directly into your development workflow. Generate dialogue, audio, and cutscenes without leaving the editor. Features include real-time preview, asset pipeline integration, and batch processing for large-scale content creation.
							</p>
							<span class="bg-gray-100 text-[10px] px-1.5 py-0.5 rounded text-muted">Product Release</span>
						</div>
					</div>

					<!-- Update 2 -->
					<div class="flex gap-8 group">
						<div class="font-mono text-xs text-muted w-24 shrink-0 pt-1">January 8</div>
						<div>
							<h3 class="font-medium text-sm mb-2 group-hover:text-accent transition-colors cursor-pointer">Video Generation Model v3.0</h3>
							<p class="text-xs text-muted leading-relaxed mb-3">
								Our latest video generation model delivers 40% better consistency for character appearances and 2x faster rendering times. Now supporting 4K output with improved temporal coherence for cinematic cutscenes. Beta testing with select AAA partners showed 85% reduction in post-production time.
							</p>
							<div class="flex gap-2">
								<span class="bg-gray-100 text-[10px] px-1.5 py-0.5 rounded text-muted">Model Update</span>
								<span class="bg-gray-100 text-[10px] px-1.5 py-0.5 rounded text-muted">Performance</span>
							</div>
						</div>
					</div>

					<!-- Update 3 -->
					<div class="flex gap-8 group">
						<div class="font-mono text-xs text-muted w-24 shrink-0 pt-1">December 20</div>
						<div>
							<h3 class="font-medium text-sm mb-2 group-hover:text-accent transition-colors cursor-pointer">Unity Asset Store Integration</h3>
							<p class="text-xs text-muted leading-relaxed mb-3">
								Core Flow is now available on the Unity Asset Store. Our plugin supports Unity 2022 LTS and newer, with full support for HDRP and URP rendering pipelines. Get started with pre-built templates for dialogue systems, audio management, and cutscene generation.
							</p>
							<span class="bg-gray-100 text-[10px] px-1.5 py-0.5 rounded text-muted">Integration</span>
						</div>
					</div>

					<!-- Update 4 -->
					<div class="flex gap-8 group">
						<div class="font-mono text-xs text-muted w-24 shrink-0 pt-1">December 1</div>
						<div>
							<h3 class="font-medium text-sm mb-2 group-hover:text-accent transition-colors cursor-pointer">Reaching 1,000+ Game Studios</h3>
							<p class="text-xs text-muted leading-relaxed mb-3">
								Core Flow now powers content generation for over 1,000 indie and mid-tier game studios worldwide, processing 10M+ generation requests monthly. Our pay-per-generation model has helped studios reduce content creation costs by an average of 60%.
							</p>
							<span class="bg-gray-100 text-[10px] px-1.5 py-0.5 rounded text-muted">Milestone</span>
						</div>
					</div>
				</div>
			</div>

		</div>
	</div>
</section>
