<template>
	<div id="app" class="xl:mx-44 lg:mx-24 sm:mx-8">
		<div class="h-16 flex">
			<div class="my-auto">
				<h2 class="text-md breadcrumbs">Home > Backpacks > {{ name }}</h2>
			</div>
		</div>

		<div class="grid grid-cols-12 grid-flow-col gap-4 mb-8">
			<div
				class="thumbnails col-span-1 max-h-screen min-h-screen overflow-y-scroll"
			>
				<div class="thumbnail-image" v-for="index in 6" :key="index">
					<a :href="`#gallery${index}`">
						<img
							:class="index !== 6 ? 'pb-3' : ''"
							:src="`https://picsum.photos/seed/${index}a/150`"
						/>
					</a>
				</div>
			</div>
			<div class="gallery col-span-8 max-h-screen min-h-screen overflow-y-scroll">
				<div class="gallery-image" v-for="index in 6" :key="index">
					<a :id="`gallery${index}`" />
					<img
						:class="index !== 6 ? 'pb-3' : ''"
						:src="`https://picsum.photos/seed/${index}a/1200/800`"
					/>
				</div>
			</div>
			<div class="col-span-3 text-left px-4">
				<h1 class="text-xl product-name mb-4">{{ name }}</h1>
				<h2 class="text-lg font-bold">$168.99</h2>
				<div class="stars mb-4">
					<span class="star" v-for="index in 5" :key="index">★</span>
				</div>
				<p class="">
					Filler text to expand this panel further down the page. Lorem ipsum dolor
					sit amet, consectetur adipiscing elit. Mauris felis sem, consequat sit amet
					nisi id, blandit finibus lectus. Suspendisse ullamcorper eros sit amet arcu
					egestas, sed fringilla erat egestas. Aenean nulla ligula, interdum et neque
					ac, tempor ornare neque. Suspendisse sed tempor sem. Nulla ultrices orci
					vel ipsum gravida, in varius turpis commodo. Morbi convallis turpis nunc,
					vel feugiat elit aliquet vitae. Nam tincidunt sapien non erat pretium
					finibus. Sed eu luctus sapien. Nullam in enim rhoncus nisl posuere varius.
					Aenean cursus purus libero, dictum scelerisque urna sagittis at. Vestibulum
					egestas nisi vel nunc sagittis, id varius libero facilisis. Morbi sagittis
					in nibh vel efficitur.
					<br />
					<br />
					<button class="toggle" @click="longText = !longText">{{longText ? 'Collapse' : 'Expand'}} Sidebar Contents</button>
					<br />
					<br />
					<p :class="longText ? '' : 'hidden'">
						Quisque cursus, metus at lobortis imperdiet, lectus augue sollicitudin
					nisl, rutrum ullamcorper elit erat quis libero. Nulla mattis, tellus quis
					convallis molestie, enim neque faucibus felis, nec egestas turpis libero
					vel augue. Morbi venenatis pharetra diam, gravida varius nunc mollis
					semper. Nunc scelerisque erat sed ligula venenatis bibendum. Nullam aliquam
					tincidunt velit, eu sodales mauris porttitor quis. Curabitur et condimentum
					elit. In consectetur urna ac tristique pellentesque. Pellentesque varius
					dolor in mollis maximus. Donec quis luctus tellus, in mattis neque.
					<br />
					<br />
					Donec tincidunt porta enim eu euismod. Cras faucibus nisl et ante pulvinar,
					at lacinia ex condimentum. Mauris non eros eu nisl tincidunt dapibus.
					Pellentesque habitant morbi tristique senectus et netus et malesuada fames
					ac turpis egestas. In hac habitasse platea dictumst. Nulla id lectus vel ex
					porttitor fringilla in sit amet erat. Cras ac ullamcorper ipsum, a pharetra
					lectus. Nullam vitae elit blandit, posuere arcu at, blandit orci. Phasellus
					porta sollicitudin eleifend. Vivamus sit amet placerat erat. Aliquam
					tincidunt quam non urna euismod, ac convallis augue lobortis. Maecenas
					dictum, magna vel pretium vestibulum, dui turpis gravida purus, eget
					euismod sapien felis in ligula. Phasellus in erat risus. Ut consequat
					libero non turpis pellentesque, eu ultricies elit consectetur. Donec congue
					arcu neque, ut luctus lectus sollicitudin id. Aenean imperdiet consectetur
					ullamcorper. Proin consectetur nec metus eu malesuada. Pellentesque mollis
					turpis augue, eget suscipit elit finibus quis. Nam eget elit sollicitudin,
					tempus metus at, consequat libero. Aliquam fringilla, dui non congue
					consequat, orci urna tincidunt arcu, eget rhoncus erat nulla eu enim.
					Nullam blandit ex at leo molestie, nec commodo augue maximus. Vestibulum
					vulputate molestie vulputate.
					<br />
					<br />
					Donec nulla ante, aliquet non auctor ut, ultricies nec lacus. Nulla sit
					amet ipsum pharetra, maximus sem nec, posuere quam. Aenean rhoncus lacus
					non nisl euismod hendrerit. Morbi tempus condimentum tortor sed pulvinar.
					Sed a risus id lorem volutpat condimentum. Cras vel eros vitae mi facilisis
					interdum a convallis tortor. Integer elementum feugiat eleifend. Morbi eget
					felis sed nibh egestas mollis ac et erat.
					</p>
				</p>
				<button
					class="add-to-cart flex justify-center uppercase text-white bg-gray-900 h-14 w-full p-4 my-8"
				>
					Add to Cart
				</button>
			</div>
		</div>
		<hr class="mb-6" />
		<div>
			<h1 class="text-xl text-left mb-6">More Content Here</h1>
			<img class="max-w-full mb-8" src="https://picsum.photos/2000/800" />
		</div>
	</div>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  color: #2c3e50;
}
</style>

<script>
export default {
  data() {
    return {
      longText: true,
      name: "Apex 3L Backpack",
      images: [
        {
          id: 1,
          url: "test.jpg",
        },
      ],
    };
  },
};
</script>
