<template>
	<div class="bg-white">
		<div class="max-w-7xl mx-auto py-16 px-4 sm:px-6 lg:py-24 lg:px-8">
			<div class="divide-y-2 divide-gray-200">
				<div class="lg:grid lg:grid-cols-3 lg:gap-8">
					<h2 class="text-2xl font-extrabold text-gray-900 sm:text-3xl">
						Get in touch
					</h2>
					<div
						class="mt-8 grid grid-cols-1 gap-12 sm:grid-cols-2 sm:gap-x-8 sm:gap-y-12 lg:mt-0 lg:col-span-2"
					>
						<div v-for="(item, index) in contact.getInTouch" :key="index">
							<h3 class="text-lg leading-6 font-medium text-gray-900">
								{{ item.event }}
							</h3>
							<dl class="mt-2 text-base text-gray-500">
								<div>
									<dt class="sr-only">
										Email
									</dt>
									<dd>
										{{ item.email }}
									</dd>
								</div>
								<div class="mt-1">
									<dt class="sr-only">
										Phone number
									</dt>
									<dd>
										{{ item.contact }}
									</dd>
								</div>
							</dl>
						</div>
					</div>
				</div>
				<div class="mt-16 pt-16 lg:grid lg:grid-cols-3 lg:gap-8">
					<h2 class="text-2xl font-extrabold text-gray-900 sm:text-3xl">
						Locations
					</h2>
					<div
						class="mt-8 grid grid-cols-1 gap-12 sm:grid-cols-2 sm:gap-x-8 sm:gap-y-12 lg:mt-0 lg:col-span-2"
					>
						<div v-for="(location, index) in contact.locations" :key="index">
							<h3 class="text-lg leading-6 font-medium text-gray-900">
								{{ location.location }}
							</h3>
							<div class="mt-2 text-base text-gray-500">
								<p>
									{{ location.addressStreet }}
								</p>
								<p class="mt-1">
									{{ location.addressCountry }}
								</p>
							</div>
						</div>
					</div>
				</div>
			</div>
		</div>
	</div>
</template>

<script>
export default {
	name: 'Contact2',
	data() {
		return {
			contact: {
				getInTouch: [
					{
						event: 'Collaborate',
						email: 'support@example.com',
						contact: '+1 (555) 123-4567',
					},
					{
						event: 'Press',
						email: 'support@example.com',
						contact: '+1 (555) 123-4567',
					},
					{
						event: 'Join Our Team',
						email: 'support@example.com',
						contact: '+1 (555) 123-4567',
					},
					{
						event: 'Say Hello',
						email: 'support@example.com',
						contact: '+1 (555) 123-4567',
					},
				],
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
			},
		};
	},
};
</script>
