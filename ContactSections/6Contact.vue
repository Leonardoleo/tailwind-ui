<!-- This example requires Tailwind CSS v2.0+ -->
<template>
	<div class="bg-white">
		<div class="max-w-7xl mx-auto py-24 px-4 sm:py-32 sm:px-6 lg:px-8">
			<h2 class="text-3xl font-extrabold text-gray-900">Our offices</h2>
			<p class="mt-6 text-lg text-gray-500 max-w-3xl">
				Varius facilisi mauris sed sit. Non sed et duis dui leo, vulputate id
				malesuada non. Cras aliquet purus dui laoreet diam sed lacus, fames.
			</p>
			<div class="mt-10 grid grid-cols-1 gap-10 sm:grid-cols-2 lg:grid-cols-4">
				<div v-for="(location, index) in locations" :key="index">
					<h3 class="text-lg font-medium text-gray-900">
						{{ location.location }}
					</h3>
					<p class="mt-2 text-base text-gray-500">
						<span class="block">
							{{ location.addressStreet }}
						</span>
						<span class="block">
							{{ location.addressCountry }}
						</span>
					</p>
				</div>
			</div>
		</div>
	</div>
</template>

<script>
export default {
	data() {
		return {
			locations: [
				{
					location: 'Los Angeles',
					addressStreet: '4556 Brendan Ferry',
					addressCountry: 'Los Angeles, CA 90210',
				},
				{
					location: 'New York',
					addressStreet: '886 Walter Streets',
					addressCountry: 'New York, NY 12345',
				},
				{
					location: 'Toronto',
					addressStreet: '7363 Cynthia Pass',
					addressCountry: 'Toronto, ON N3Y 4H8',
				},
				{
					location: 'Chicago',
					addressStreet: '726 Mavis Island',
					addressCountry: 'Chicago, IL 60601',
				},
			],
		};
	},
};
</script>
