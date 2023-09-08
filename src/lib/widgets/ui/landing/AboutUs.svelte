<script>
	const aboutUsData = [
		"Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it make a type specimen book.",
		"Lorem Ipsum has been the industry's standard dummy text ever since the 1700s, when an unknown printer took a galley of type and scrambled it make a type specimen book."
	];
</script>

<div
	class="mt-11 flex w-full flex-col-reverse items-center justify-between gap-16 px-5 sm:mt-0 sm:px-[50px] md:flex-row md:gap-4"
>
	<a name="about" />

	<div class="relative">
		<img
			src="/images/about.png"
			class="relative !z-40 h-[278px] sm:h-[462px] md:h-full"
			alt="about us"
		/>
	</div>
	<div class="flex flex-col items-center justify-start gap-5 md:items-start">
		<div
			class="ont-hindVadodara relative flex flex-col text-4xl leading-[106.3%] -tracking-[0.01] text-[#331B3B] md:mt-32 lg:text-5xl"
		>
			<h1 class=" text-center font-bold md:text-left">About Us</h1>
			<span class="text-4xl font-light lg:text-5xl">
				Fake or
				<span class="relative z-10 ml-3">
					Real
					<span
						class="absolute bottom-[10px] left-0 -z-[1] h-2 w-full bg-primary lg:bottom-[14px]"
					/>
				</span>
			</span>
		</div>
		<div class="flex flex-col gap-2">
			{#each aboutUsData as about}
				<span
					class="Light font-hindVadodara mt-[6px] max-w-[515px] text-center text-[15px] font-light leading-[145.3%] tracking-[0.02] md:text-left"
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
