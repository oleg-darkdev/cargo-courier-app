<script>
	const partners = [
		{
			title: 'Lorem Ipsum',
			img: '/images/',
			desc: 'Lorem Ipsum has been the industry&apos;s standard dummy text ever since the 1500s.'
		}
	];
</script>

<div class="relative mt-12 h-[725px] w-full overflow-hidden py-24 md:mt-20 md:h-[636px]">
	<div
		class="absolute top-0 right-0 z-10 ml-3 h-full w-full max-w-[1300px] rounded-tl-[137px] bg-primary sm:rounded-tl-[400px]"
	/>
	<div class="absolute top-0 !z-30 flex h-full w-full flex-col gap-24 py-24 md:py-40">
		<div class=" mx-auto flex flex-col gap-8 sm:gap-10 md:gap-24">
			<div class="mx-5 flex flex-col gap-5">
				<div class="relative md:absolute md:left-5 md:top-10 lg:left-32">
					<h1
						class="font-hindVadodara self-center text-3xl font-bold leading-[106.3%] -tracking-[0.01] text-secondary lg:text-5xl"
					>
						Our Partners
						<p />
						<span class="font-light">
							Lorem
							<span class="relative z-10">
								Lorem
								<span
									class="absolute bottom-1.5 right-0 -z-[1] h-2 w-[104px] bg-primary lg:bottom-[9px] lg:w-40"
								/>
							</span>
						</span>
					</h1>
				</div>
				<span
					class="relative w-full max-w-md text-lg font-normal text-secondary md:absolute md:right-12 md:top-10 xl:max-w-lg"
				>
					Lorem ipsum dolor sit amet consectetur, adipisicing elit. Nobis, aperiam facere labore
					ipsum, vitae impedit temporibus ratione quae laborum itaque harum nihil maiores doloremque
					minus debitis et nisi explicabo non.
				</span>
			</div>
			<div class="flex gap-12 px-5 sm:pl-8 lg:pl-64">
				<div class="hidden items-end gap-4 md:flex">
					<svg
						width="35"
						height="34"
						viewBox="0 0 35 34"
						fill="none"
						xmlns="http://www.w3.org/2000/svg"
						class="rotate-180 cursor-pointer"
						on:click={() => console.log('moveLeft(workSlider)')}
					>
						<path
							d="M1 17C1 25.8094 8.35978 33 17.5 33C26.6402 33 34 25.8094 34 17C34 8.19057 26.6402 1 17.5 1C8.35978 1 1 8.19057 1 17Z"
							stroke="black"
							strokeWidth="2"
						/>
						<path
							d="M15 10L23 17.3443L15 24"
							stroke="black"
							strokeWidth="2"
							strokeLinecap="round"
						/>
					</svg>
					<svg
						width="35"
						height="34"
						viewBox="0 0 35 34"
						fill="none"
						xmlns="http://www.w3.org/2000/svg"
						class="cursor-pointer"
						on:click={() => console.log('moveRight(workSlider)')}
					>
						<path
							d="M1 17C1 25.8094 8.35978 33 17.5 33C26.6402 33 34 25.8094 34 17C34 8.19057 26.6402 1 17.5 1C8.35978 1 1 8.19057 1 17Z"
							stroke="black"
							strokeWidth="2"
						/>
						<path
							d="M15 10L23 17.3443L15 24"
							stroke="black"
							strokeWidth="2"
							strokeLinecap="round"
						/>
					</svg>
				</div>
				<div class="dream-agency-work flex">
					{#each partners as card}
						<div
							class="shadow-3xl w-full max-w-lg justify-start self-center rounded-[10px] bg-white p-[18px]"
						>
							<div class="h-full">
								<img scr={card.img} alt="card image" class="h-48 w-full object-cover" />
							</div>
							<div class="mt-5 flex justify-between">
								<span class="text-2xl font-bold text-secondary">
									{card.title}
								</span>
								<div
									class="h-max w-28 cursor-pointer whitespace-nowrap rounded-[100px] border-[2px] border-[#343434] py-0.5 px-3 text-center text-sm"
								>
									View work
								</div>
							</div>
						</div>
					{/each}

					<!-- <Slider {...workSliderSetting} ref={workSlider}>

                    </Slider> -->
				</div>
			</div>
		</div>
	</div>
</div>
