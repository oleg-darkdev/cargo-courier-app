<script>
	const aboutUsData = [
		`Projekt rozpoczął się w 2023 roku w Gdańsku, w Polsce. Projekt został założony przez grupę uchodźców politycznych z Białorusi.`,

		`Nasz cel: zmniejszenie śladu węglowego w świecie transportu towarów poprzez oferowanie dostaw towarów na rowerze dla firm i wsparcie organizacji non-profit.`,
		`Pasjonaci środowiska i mobilności miejskiej postanowili zmienić podejście do transportu towarów. Dążąc do stworzenia bardziej przyjaznego dla środowiska i zrównoważonego systemu dostaw - zdecydowaliśmy się wprowadzić rowery towarowe do infrastruktury miejskiej.`,
		`Nasza oferta to coś więcej niż tylko transport ciężarowy, zapraszamy do przyłączenia się do ruchu, który łączy środowisko, sprawiedliwość społeczną i elastyczne podejście do biznesu.`,
		`Zapraszamy do wsparcia naszej inicjatywy i uczynienia naszego świata czystszym i bardziej ekologicznym razem z nami.`
	];
</script>

<a name="about" />

<div data-aos="fade-left"
	class="mt-11 flex w-full flex-col-reverse items-center justify-between gap-16 px-5 sm:mt-0 sm:px-[50px] md:flex-row md:gap-4"
>
	<div class="relative">
		<img
			src="/images/about.png"
			class="relative !z-40 h-[278px] sm:h-[462px] md:h-full"
			alt="about us"
		/>
	</div>
	<div class="flex flex-col items-center justify-start gap-5 md:items-start">
		<div
			class="ont-hindVadodara relative flex flex-col text-4xl leading-[106.3%] -tracking-[0.01] text-secondary md:mt-32 lg:text-5xl"
		>
			<h1 class=" text-center font-bold md:text-left">O nas</h1>
			<span class="text-4xl font-light lg:text-5xl">
				Więcej niż tylko
				<span class="relative z-10 ml-3">
					Transport
					<span
						class="absolute bottom-[10px] left-0 -z-[1] h-2 w-full bg-primary lg:bottom-[14px]"
					/>
				</span>
			</span>
		</div>
		<div class="flex flex-col gap-2">
			{#each aboutUsData as about}
				<span
					class=" font-hindVadodara mt-[6px] max-w-[515px] text-center text-[15px] font-bold leading-[145.3%] tracking-[0.02] text-secondary md:text-left"
				>
					{about}
				</span>
			{/each}
		</div>
		<div class="mt-2 md:mt-10">
			<!-- <Button
                  class="whitespace-nowrap max-w-[207px] py-[22px] w-full flex justify-center items-center font-bold leading-[137.3%] tracking-wide px-10"
                  label="Explore More"
                />

                <button
        class={`bg-secondary rounded-[10px] text-[17px] text-white uppercase font-hindVadodara ${class}`}
        on:click={on:click}
      >
        {label}
      </button> -->
		</div>
	</div>
</div>
