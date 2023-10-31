<script>
	const testimonialsCard = [
		{
			title: 'UI Soup',
			discription:
				"Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries."
		},
		{
			title: 'UI Soup',
			discription:
				"Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries."
		}
	];
</script>

<div class="mt-9 flex w-full flex-col items-center justify-center gap-14 px-5 md:mt-[75px]">
	<div
		class=" font-hindVadodara w-full text-center text-3xl -tracking-[0.01em] text-secondary md:text-5xl"
	>
		<h1 class="whitespace-nowrap text-center font-bold leading-[99.8%]">Our Testimonials</h1>
		<span class="mx-auto mt-1 max-w-sm !text-center font-light md:max-w-xl md:whitespace-nowrap">
			What Our Clients Are
			<span class="relative z-10 ml-2">
				Saying
				<span
					class="absolute bottom-1 right-[100px] left-0 -z-[1] h-2 w-full bg-primary sm:right-0 md:bottom-2"
				/>
			</span>
		</span>
	</div>
	<div class="flex flex-col gap-7 sm:gap-[69px] md:flex-row">
		{#each testimonialsCard as data}
			<div
				class="flex flex-col justify-start gap-7 bg-secondary py-9 pl-[29px] pr-[35px] drop-shadow-[0_7px_9px_rgba(0,0,0,0.15)]"
			>
				<div>
					<svg
						width="46"
						height="40"
						viewBox="0 0 46 40"
						fill="none"
						xmlns="http://www.w3.org/2000/svg"
					>
						<path
							d="M35.4128 39.5905L45.4 18.5185V0.409668H24.9856V19.6161H32.7776L24.9856 39.5905H35.4128ZM28.0336 16.5681V3.45927H42.3504V17.8321L33.4816 36.5409H29.4464L37.2352 16.5697H28.0336V16.5681Z"
							fill="#8ad288"
						/>
						<path
							d="M11.0272 39.5905L21.0144 18.5185V0.409668H0.600006V19.6161H8.39361L0.600006 39.5905H11.0272ZM3.64801 16.5681V3.45927H17.9648V17.8321L9.09761 36.5409H5.06241L12.8512 16.5697H3.64801V16.5681Z"
							fill="#8ad288"
						/>
					</svg>
				</div>
				<div class="flex flex-col justify-start gap-3">
					<span
						class=" font-hindVadodara w-full max-w-[384px] text-base font-normal leading-[159.8%] tracking-wide"
					>
						{data.discription}
					</span>
					<span
						class="font-hindVadodara flex items-center gap-2 text-base font-semibold leading-[159.8%] tracking-wide"
					>
						<span class=" relative bottom-0.5 w-3 border-[2px] border-[#8ad288]" />
						{data.title}
					</span>
				</div>
			</div>
		{/each}
	</div>
</div>
