<script>
	let showMenu = false;
	// '', '', '', ''
	const navList = [
		{
			link: '#bussines',
			title: 'Dla Biznesu'
		},
		{
			link: '#ngo',
			title: 'Dla NGO'
		},
		{
			link: '#about',
			title: 'O nas'
		},
		{
			link: '#shop',
			title: 'Sklep'
		},

		{
			link: '#contact',
			title: 'Contact Us'
		}
	];
	$: active = '';
</script>

<nav class=" absolute top-0 left-0 z-20 w-full rounded-br-[80px]  bg-primary sm:px-4  lg:w-5/12">
	<div class="container  w-full">
		<nav
			class="relative   mx-auto flex  items-center justify-between px-5 py-[26.36px] sm:px-[50px]"
		>
			<ul
				class="font-hindVadodara hidden items-center gap-5 text-base font-normal leading-6 tracking-[0.01] md:flex lg:gap-8 xl:gap-12"
			>
				{#each navList as item}
					<li on:click={() => (active = item)} class="relative z-10 cursor-pointer text-secondary ">
						<!--  -->
						<a href={item.link}>
							{item.title}
							<span
								class="absolute bottom-[2px] -left-0.5 -z-[1] h-2 bg-primary text-secondary
                    {active === item ? 'w-full' : 'w-0'} "
							/>
						</a>
					</li>
				{/each}
			</ul>
			<!-- <div class="cursor-pointer xl:mr-56">
				<p class="font-playFairDisplay text-2xl font-bold leading-7 tracking-[0.01] text-secondary">
					Cargo Courier Collective
				</p>
			</div> -->
			<!--
			<ul class="hidden items-center gap-4 md:flex">
				<div class="relative z-20 cursor-pointer">
					<svg
						width="46"
						height="49"
						viewBox="0 0 46 49"
						fill="none"
						xmlns="http://www.w3.org/2000/svg"
					>
						<path
							d="M40.7347 35.3674C37.8086 40.3349 32.7551 44.2964 27.1723 46.2689C21.5909 48.2409 15.5957 48.1894 10.7238 45.3196C5.8519 42.4498 2.90043 37.2311 1.91937 31.3935C0.938064 25.5544 1.95301 19.2139 4.87912 14.2465C7.80523 9.27901 12.8587 5.31748 18.4415 3.34498C24.0229 1.37298 30.0181 1.42444 34.89 4.29427C39.7619 7.16409 42.7134 12.3827 43.6945 18.2204C44.6758 24.0595 43.6608 30.4 40.7347 35.3674Z"
							stroke="#111827"
							strokeOpacity="0.64"
							strokeWidth="2"
						/>
					</svg>
					<div class="absolute top-4 left-4 cursor-pointer">
						<svg
							width="11"
							height="21"
							viewBox="0 0 11 21"
							fill="none"
							xmlns="http://www.w3.org/2000/svg"
						>
							<g clipPath="url(#clip0_8_35)">
								<path
									fillRule="evenodd"
									clipRule="evenodd"
									d="M7.62817 20.8071V11.8071H10.3606L10.8069 7.80713H7.62817V5.85889C7.62817 4.82889 7.65449 3.80713 9.09378 3.80713H10.5516V0.947266C10.5516 0.904266 9.29937 0.807129 8.03256 0.807129C5.38688 0.807129 3.73029 2.46432 3.73029 5.50732V7.80713H0.806885V11.8071H3.73029V20.8071H7.62817Z"
									fill="#111827"
								/>
							</g>
							<defs>
								<clipPath id="clip0_8_35">
									<rect
										width="10"
										height="20"
										fill="white"
										transform="translate(0.806885 0.807129)"
									/>
								</clipPath>
							</defs>
						</svg>
					</div>
				</div>
				<div class="relative z-20 cursor-pointer">
					<svg
						width="46"
						height="49"
						viewBox="0 0 46 49"
						fill="none"
						xmlns="http://www.w3.org/2000/svg"
					>
						<path
							d="M40.7347 35.3674C37.8086 40.3349 32.7551 44.2964 27.1723 46.2689C21.5909 48.2409 15.5957 48.1894 10.7238 45.3196C5.8519 42.4498 2.90043 37.2311 1.91937 31.3935C0.938064 25.5544 1.95301 19.2139 4.87912 14.2465C7.80523 9.27901 12.8587 5.31748 18.4415 3.34498C24.0229 1.37298 30.0181 1.42444 34.89 4.29427C39.7619 7.16409 42.7134 12.3827 43.6945 18.2204C44.6758 24.0595 43.6608 30.4 40.7347 35.3674Z"
							stroke="#111827"
							strokeOpacity="0.64"
							strokeWidth="2"
						/>
					</svg>
					<div class="absolute top-4 left-4">
						<svg
							width="19"
							height="19"
							viewBox="0 0 19 19"
							fill="none"
							xmlns="http://www.w3.org/2000/svg"
						>
							<g clipPath="url(#clip0_8_42)">
								<path
									fillRule="evenodd"
									clipRule="evenodd"
									d="M18.2566 18.8071H14.5582V12.5079C14.5582 10.7808 13.9019 9.81562 12.5349 9.81562C11.0478 9.81562 10.2709 10.82 10.2709 12.5079V18.8071H6.70659V6.80713H10.2709V8.42353C10.2709 8.42353 11.3425 6.44051 13.889 6.44051C16.4343 6.44051 18.2566 7.99483 18.2566 11.2095V18.8071ZM2.45444 5.23582C1.24038 5.23582 0.256592 4.24432 0.256592 3.02148C0.256592 1.79864 1.24038 0.807129 2.45444 0.807129C3.6685 0.807129 4.6517 1.79864 4.6517 3.02148C4.6517 4.24432 3.6685 5.23582 2.45444 5.23582ZM0.614017 18.8071H4.33062V6.80713H0.614017V18.8071Z"
									fill="#111827"
								/>
							</g>
							<defs>
								<clipPath id="clip0_8_42">
									<rect
										width="18"
										height="18"
										fill="white"
										transform="translate(0.256592 0.807129)"
									/>
								</clipPath>
							</defs>
						</svg>
					</div>
				</div>
				<div class="relative z-20 cursor-pointer">
					<svg
						width="46"
						height="49"
						viewBox="0 0 46 49"
						fill="none"
						xmlns="http://www.w3.org/2000/svg"
					>
						<path
							d="M40.7347 35.3674C37.8086 40.3349 32.7551 44.2964 27.1723 46.2689C21.5909 48.2409 15.5957 48.1894 10.7238 45.3196C5.8519 42.4498 2.90043 37.2311 1.91937 31.3935C0.938064 25.5544 1.95301 19.2139 4.87912 14.2465C7.80523 9.27901 12.8587 5.31748 18.4415 3.34498C24.0229 1.37298 30.0181 1.42444 34.89 4.29427C39.7619 7.16409 42.7134 12.3827 43.6945 18.2204C44.6758 24.0595 43.6608 30.4 40.7347 35.3674Z"
							stroke="#111827"
							strokeOpacity="0.64"
							strokeWidth="2"
						/>
					</svg>
					<div class="absolute top-3 left-3">
						<svg
							width="25"
							height="25"
							viewBox="0 0 25 25"
							fill="none"
							xmlns="http://www.w3.org/2000/svg"
						>
							<g clipPath="url(#clip0_8_46)">
								<path
									d="M12.7065 3.12733C15.8612 3.12733 16.2315 3.14139 17.4784 3.19764C18.6315 3.24921 19.2549 3.44139 19.6721 3.60546C20.2252 3.82108 20.619 4.07421 21.0315 4.48671C21.444 4.89921 21.7018 5.29296 21.9127 5.84608C22.0721 6.26327 22.269 6.88671 22.3206 8.03983C22.3768 9.28671 22.3909 9.65702 22.3909 12.8117C22.3909 15.9664 22.3768 16.3367 22.3206 17.5836C22.269 18.7367 22.0768 19.3601 21.9127 19.7773C21.6971 20.3305 21.444 20.7242 21.0315 21.1367C20.619 21.5492 20.2252 21.807 19.6721 22.018C19.2549 22.1773 18.6315 22.3742 17.4784 22.4258C16.2315 22.482 15.8612 22.4961 12.7065 22.4961C9.55181 22.4961 9.18149 22.482 7.93462 22.4258C6.78149 22.3742 6.15806 22.182 5.74087 22.018C5.18774 21.8023 4.79399 21.5492 4.38149 21.1367C3.96899 20.7242 3.71118 20.3305 3.50024 19.7773C3.34087 19.3601 3.14399 18.7367 3.09243 17.5836C3.03618 16.3367 3.02212 15.9664 3.02212 12.8117C3.02212 9.65702 3.03618 9.28671 3.09243 8.03983C3.14399 6.88671 3.33618 6.26327 3.50024 5.84608C3.71587 5.29296 3.96899 4.89921 4.38149 4.48671C4.79399 4.07421 5.18774 3.81639 5.74087 3.60546C6.15806 3.44608 6.78149 3.24921 7.93462 3.19764C9.18149 3.13671 9.55181 3.12733 12.7065 3.12733ZM12.7065 0.999207C9.50024 0.999207 9.09712 1.01327 7.83618 1.06952C6.57993 1.12577 5.72212 1.32733 4.97212 1.61796C4.19399 1.91796 3.53774 2.32577 2.88149 2.98202C2.22524 3.63827 1.82212 4.29921 1.51743 5.07264C1.22681 5.82264 1.02524 6.68046 0.968994 7.94139C0.912744 9.19764 0.898682 9.60077 0.898682 12.807C0.898682 16.0133 0.912744 16.4164 0.968994 17.6773C1.02524 18.9336 1.22681 19.7914 1.51743 20.5461C1.81743 21.3242 2.22524 21.9805 2.88149 22.6367C3.53774 23.293 4.19868 23.6961 4.97212 24.0008C5.72212 24.2914 6.57993 24.493 7.84087 24.5492C9.10181 24.6055 9.50024 24.6195 12.7112 24.6195C15.9221 24.6195 16.3206 24.6055 17.5815 24.5492C18.8377 24.493 19.6956 24.2914 20.4502 24.0008C21.2284 23.7008 21.8846 23.293 22.5409 22.6367C23.1971 21.9805 23.6002 21.3195 23.9049 20.5461C24.1956 19.7961 24.3971 18.9383 24.4534 17.6773C24.5096 16.4164 24.5237 16.018 24.5237 12.807C24.5237 9.59608 24.5096 9.19764 24.4534 7.93671C24.3971 6.68046 24.1956 5.82264 23.9049 5.06796C23.6049 4.28983 23.1971 3.63358 22.5409 2.97733C21.8846 2.32108 21.2237 1.91796 20.4502 1.61327C19.7002 1.32264 18.8424 1.12108 17.5815 1.06483C16.3159 1.01327 15.9127 0.999207 12.7065 0.999207Z"
									fill="#111827"
								/>
								<path
									d="M12.7065 6.74139C9.35962 6.74139 6.64087 9.45546 6.64087 12.807C6.64087 16.1586 9.35962 18.8726 12.7065 18.8726C16.0534 18.8726 18.7721 16.1539 18.7721 12.807C18.7721 9.46014 16.0534 6.74139 12.7065 6.74139ZM12.7065 16.7445C10.5315 16.7445 8.76899 14.982 8.76899 12.807C8.76899 10.632 10.5315 8.86952 12.7065 8.86952C14.8815 8.86952 16.644 10.632 16.644 12.807C16.644 14.982 14.8815 16.7445 12.7065 16.7445Z"
									fill="#111827"
								/>
								<path
									d="M19.0112 7.91798C19.793 7.91798 20.4268 7.28418 20.4268 6.50236C20.4268 5.72053 19.793 5.08673 19.0112 5.08673C18.2294 5.08673 17.5956 5.72053 17.5956 6.50236C17.5956 7.28418 18.2294 7.91798 19.0112 7.91798Z"
									fill="#111827"
								/>
							</g>
							<defs>
								<clipPath id="clip0_8_46">
									<rect
										width="24"
										height="24"
										fill="white"
										transform="translate(0.706543 0.807129)"
									/>
								</clipPath>
							</defs>
						</svg>
					</div>
				</div>
			</ul>
			<ul class="block h-10 w-12 md:hidden">
				<svg
					xmlns="http://www.w3.org/2000/svg"
					width="1em"
					height="1em"
					viewBox="0 0 16 16"
					on:click={() => console.log('yeap')}
					class=" h-10 w-12"
				>
					<path
						fill="none"
						stroke="currentColor"
						strokeLinecap="round"
						strokeLinejoin="round"
						strokeWidth="1.5"
						d="M2.75 12.25h10.5m-10.5-4h10.5m-10.5-4h10.5"
					/>
				</svg>
			</ul>
			<img
				scr="/images/home.png"
				alt="Home"
				class="absolute -right-56 -top-20 hidden h-[362px] w-[450px] md:block lg:h-full xl:-right-10 xl:top-0"
			/> -->

			<div
				class="z-50 transition-all ease-in-out
			{showMenu
					? 'fixed left-0 top-0 flex h-max min-h-screen w-full flex-col bg-[#2D4263] md:hidden'
					: 'fixed top-0 left-full flex h-screen w-full flex-col bg-[#2D4263] md:hidden'}"
			>
				<div
					class="flex w-full items-center justify-end px-[10%] pt-5 text-xl font-bold"
					on:click={() => (showMenu = !showMenu)}
				>
					<img src="" alt="close" class="h-7 cursor-pointer" />
				</div>
				<div
					class="flex h-screen w-full flex-col items-center justify-center gap-[30px] text-[20px] font-normal leading-[29px] sm:gap-[50px] sm:text-lg md:hidden md:flex-row md:gap-[60px]"
				>
					{#each navList as item}
						<div
							class="font-hindVadodara cursor-pointer text-2xl font-normal leading-6 tracking-[0.01] text-white"
						>
							{item}
						</div>
					{/each}
				</div>
			</div>
		</nav>
	</div>
</nav>
