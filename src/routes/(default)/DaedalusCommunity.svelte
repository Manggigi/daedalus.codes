<script lang="ts">
	import { Container } from '@components/utilities';
	import Icon from '@iconify/svelte';
</script>

<section class="bg-surface-100-800-token py-32 dark:bg-transparent">
	<Container>
		<div class="flex flex-wrap">
			<div class="w-full pb-20 md:max-w-[50%]">
				<h2 class="text-center text-5xl font-black md:text-left md:text-6xl">
					Be a part of the
					<span class="lg:block"><span class="text-primary-600">Daedalus</span> Community</span>
				</h2>
				<img
					src="https://storage.daedalus.codes/saly.png"
					alt="thumbnail"
					class="ms-auto hidden max-w-[500px] md:block"
				/>
			</div>

			<div class="w-full md:max-w-[50%]">
				<div class="mb-20 flex">
					<Icon icon="carbon:arrow-right" class="flex-none text-4xl text-primary-600" />
					<div class="ps-5">
						<h3 class="py- mb-5 text-3xl md:text-4xl">CONNECT</h3>
						<p class="md:text-xl">
							Network, collaborate with the community members. Lorem ipsum dolor sit amet
							consectetur, Vitae enim ultricies posuere sollicitudin lacus nulla nibh sollicitudin
						</p>
					</div>
				</div>
				<div class="mb-20 flex">
					<Icon icon="carbon:arrow-right" class="flex-none text-4xl text-primary-600" />
					<div class="ps-5">
						<h3 class="mb-5 text-3xl md:text-4xl">BROWSER FREE COURSES</h3>
						<p class="md:text-xl">
							Network, collaborate with the community members. Lorem ipsum dolor sit amet
							consectetur, Vitae enim ultricies posuere sollicitudin lacus nulla nibh sollicitudin
						</p>
					</div>
				</div>
				<div class="mb-20 flex">
					<Icon icon="carbon:arrow-right" class="flex-none text-4xl text-primary-600" />
					<div class="ps-5">
						<h3 class="mb-5 text-3xl md:text-4xl">MENTORSHIP</h3>
						<p class="md:text-xl">
							Network, collaborate with the community members. Lorem ipsum dolor sit amet
							consectetur, Vitae enim ultricies posuere sollicitudin lacus nulla nibh sollicitudin
						</p>
					</div>
				</div>
			</div>

			<div class="relative -z-10 mt-[-35%] w-full opacity-70 md:max-w-[50%]">
				<img
					src="https://storage.daedalus.codes/saly.png"
					alt="thumbnail"
					class="mx-auto ms-auto block max-w-[500px] md:hidden"
				/>
			</div>
		</div>
	</Container>
</section>
