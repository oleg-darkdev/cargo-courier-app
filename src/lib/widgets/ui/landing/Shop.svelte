<script>
	import { ShopCard } from '../../../entities/';

	let products = [
		{
			img: 'https://bikepacking.com/wp-content/uploads/2020/12/tailfin-cargo-cage-foot-exploded.jpg',
			title: 'Lorem ipsum is placeholder',
			price: '$27',
			desc: [
				`Lorem ipsum is placeholder text commonly used in the graphic, print, and publishing industries for previewing layouts and visual mockups.`
			]
		},
		{
			img: 'https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Ftse2.mm.bing.net%2Fth%3Fid%3DOIP.9T6XEM_I27ZNMMk1XYRoUQHaE7%26pid%3DApi&f=1&ipt=3a808b4e8c1ba61affacbb8ef7ade140e89add6b4e0b091797b800786c5a49e7&ipo=images',
			title: 'Lorem ipsum is placeholder',
			price: '$12',
			desc: [
				`Lorem ipsum is placeholder text commonly used in the graphic, print, and publishing industries for previewing layouts and visual mockups.`
			]
		},
		{
			img: 'https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Ftse1.mm.bing.net%2Fth%3Fid%3DOIP.04euncOjLF2WWtHAwMyhZgHaFj%26pid%3DApi&f=1&ipt=c11a3a1fc520c6acceab4cf586df09af59b997dd144416bfadd0dea7a9bd887c&ipo=images',
			title: 'Lorem ipsum is placeholder',
			price: '$33',
			desc: [
				`Lorem ipsum is placeholder text commonly used in the graphic, print, and publishing industries for previewing layouts and visual mockups.`
			]
		}
		// {
		// 	img: 'https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Ftse4.mm.bing.net%2Fth%3Fid%3DOIP.aIWOB5xEzR5yS-z6BEfVKgHaHa%26pid%3DApi&f=1&ipt=ffec75e8db92e08764dab62d2d25f64a5947cf0b43cada613b87173623c87481&ipo=images',
		// 	title: 'Lorem ipsum is placeholder',
		// 	price: '$40',
		// 	desc: [
		// 		`Lorem ipsum is placeholder text commonly used in the graphic, print, and publishing industries for previewing layouts and visual mockups.`
		// 	]
		// }
	];
</script>

<a name="shop" />

<section
	class="lg:relative lg:left-20 md:left-10 left-0  flex h-auto w-full flex-row flex-wrap gap-4 lg:rounded-[80px] bg-primary py-12 lg:px-8 px-2 lg:my-0 my-6"
>
	<div class=" flex flex-col lg:gap-12 gap-2 lg:px-10 px-2 sm:gap-16 md:gap-24">
		<div
			class="font-hindVadodara mx-auto text-4xl leading-[106.3%] -tracking-[0.01] text-primary md:text-5xl"
		>
			<h1 class=" self-center text-center font-bold text-secondary">Nasz</h1>
			<span class="self-center font-light font-bold text-white">
				firmowy
				<span class="relative ml-1 font-bold   text-secondary">
					sklep <span
						class="absolute bottom-1.5 right-0 -z-[1] h-2 w-[145px] bg-white md:bottom-2 md:h-2.5 md:w-48"
					/>
				</span>
			</span>
		</div>
		<div class="flex flex-wrap flex-row gap-12 px-5 sm:pl-8 lg:pl-32">
			{#each products as productData}
				<ShopCard {productData} />
			{/each}
		</div>
	</div>
</section>
