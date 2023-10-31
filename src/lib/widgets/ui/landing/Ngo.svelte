<script>
	const cardDetail = [
		//
		{
			title: 'Bike logistics',
			img: '/images/',
			logoBg: 'bg-secondary',
			logo: '/images/websiteLogo.svg',
			desc: [
				'Cargo Courier Collective develops low-carbon quality bike logistics and fosters short supply chains in Tri-city (Gdańsk, Sopot, Gdynia).'
			]
		},
		{
			title: 'Local, fair and circular',
			img: '/images/',
			logoBg: 'bg-secondary',
			logo: '/images/websiteLogo.svg',
			desc: [
				`Cargo Courier Collective is committed to make Brussels greener by promoting a safe and renewed mobility.`,
				`We are optimizing the distribution chain for a fast, efficlient urban last-mile delivery.`
			]
		},
		// And we collect aslo food waste and leftovers for their reintroduction in the supply chain

		{
			title: 'Business co-op for social economy',
			img: '/images/',
			logoBg: 'bg-secondary',
			logo: '/images/websiteLogo.svg',
			desc: [
				' cares for its bikers-cooperators who are invited to take part into the development of the company. On a fair trade principle, we offer sustainable jobs.'
			]
		}
		// {
		// 	title: 'Lorem Ipsum',
		// 	img: '/images/',
		// 	logoBg: 'bg-secondary',
		// 	logo: '/images/websiteLogo.svg',
		// 	desc: ['Lorem Ipsum has been the industry&apos;s standard dummy text ever since the 1500s.']
		// },
		// {
		// 	title: 'Lorem Ipsum',
		// 	img: '/images/',
		// 	logoBg: 'bg-secondary',
		// 	logo: '/images/websiteLogo.svg',
		// 	desc: ['Lorem Ipsum has been the industry&apos;s standard dummy text ever since the 1500s.']
		// }
	];
</script>

<!-- lg:h-[500px]  -->
<div
	data-aos="fade-up"
	class="mt-14 w-full pb-40 h-auto mb-40 md:my-20 relative lg:overflow-hidden"
>
	<a name="ngo" />
	<!-- round -->
	<!-- <div
		class="absolute right-16 top-56 h-96 w-96 rounded-full border-[1px] border-dashed border-[#000000] p-2"
	/> -->
	<div
		class="relative top-0 right-0 z-10 mr-3 h-[500px] w-full max-w-[1293px] rounded-bl-[137px] bg-secondary sm:h-[578px] sm:rounded-bl-[400px]"
	/>
	<div class="absolute top-0 right-0 !z-30 flex h-full w-full flex-col gap-24 py-24">
		<div class=" flex flex-col gap-12 sm:gap-16 md:gap-24">
			<div
				class="font-hindVadodara mx-auto text-4xl leading-[106.3%] -tracking-[0.01] text-primary md:text-5xl"
			>
				<h2 class=" self-center text-center font-bold">Co Oferujemy</h2>
				<span class="self-center font-light text-white">
					Dla Lokalnych
					<span class="relative ml-1 font-black text-primary">
						NGO
						<span
							class="absolute bottom-1.5 right-0 -z-[1] h-2 w-[50px] bg-white md:bottom-2 md:h-2.5 md:w-32"
						/>
					</span>
				</span>
			</div>
			<div class="lg:left-20  px-5 sm:pl-8  md:relative lg:relative lg:pl-64">
				<!-- arrows for slider -->
				<!-- <div class="hidden items-end gap-4 md:flex">
						<svg
							width="35"
							height="34"
							viewBox="0 0 35 34"
							fill="none"
							xmlns="http://www.w3.org/2000/svg"
							class="rotate-180 cursor-pointer"
							on:click={() => console.log('moveLeft(bussinessSlider)')}
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
							on:click={() => console.log('moveRight(bussinessSlider)')}
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
					</div> -->
				<div class="pb-40 flex flex-row flex-wrap justify-center">
					{#each cardDetail as card}
          <!-- overflow-hidden -->
						<div
							class="shadow-3xl mb-2 mx-1 flex w-full max-w-[308px] flex-col justify-start  rounded-[10px] bg-primary p-[18px] text-secondary"
						>
							<!-- -->
							<div
								class={`{card ? 'logoBg': ''} flex h-12 w-[52px] items-center justify-center rounded-[10px] `}
							>
								<img src={card.logo} />
							</div>
							<div>
								<span
									class="font-hindVadodara mt-3 overflow-hidden text-base font-bold uppercase leading-[137.3%] -tracking-tighter"
								>
									{card.title}
								</span>
							</div>
							<div>
								{#each card.desc as desc}
									<p
										class="font-hindVadodara mt-2 h-full max-h-16  text-[15px] font-light leading-[145.3%] tracking-[0.02]"
									>
										{desc}
									</p>
								{/each}
							</div>
						</div>
					{/each}
					<!-- <Slider {...bussinessSliderSetting} ref={bussinessSlider}>

                    </Slider> -->
				</div>
			</div>
		</div>
	</div>
</div>
