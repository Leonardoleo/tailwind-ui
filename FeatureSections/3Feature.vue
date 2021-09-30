<!-- This example requires Tailwind CSS v2.0+ -->
<template>
	<div class="bg-white">
		<div class="max-w-7xl mx-auto py-16 px-4 sm:px-6 lg:py-24 lg:px-8">
			<div class="max-w-3xl mx-auto text-center">
				<h2 class="text-3xl font-extrabold text-gray-900">
					All-in-one platform
				</h2>
				<p class="mt-4 text-lg text-gray-500">
					Ac euismod vel sit maecenas id pellentesque eu sed consectetur.
					Malesuada adipiscing sagittis vel nulla nec.
				</p>
			</div>
			<dl
				class="mt-12 space-y-10 sm:space-y-0 sm:grid sm:grid-cols-2 sm:gap-x-6 sm:gap-y-12 lg:grid-cols-4 lg:gap-x-8"
			>
				<div v-for="feature in features" :key="feature.name" class="relative">
					<dt>
						<CheckIcon
							class="absolute h-6 w-6 text-green-500"
							aria-hidden="true"
						/>
						<p class="ml-9 text-lg leading-6 font-medium text-gray-900">
							{{ feature.name }}
						</p>
					</dt>
					<dd class="mt-2 ml-9 text-base text-gray-500">
						{{ feature.description }}
					</dd>
				</div>
			</dl>
		</div>
	</div>
</template>

<script>
import { CheckIcon } from '@heroicons/vue/outline';
import { computed } from 'vue';
import { useStore } from 'vuex';

export default {
	components: {
		CheckIcon,
	},
	setup() {
		const store = useStore();
		return {
			features: computed(() => store.state.feature),
		};
	},
};
</script>
