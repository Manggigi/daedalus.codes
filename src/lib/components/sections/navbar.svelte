<script lang="ts">
	import { page } from '$app/stores';
	import { AppBar, LightSwitch, getDrawerStore } from '@skeletonlabs/skeleton';
	import AvatarButton from './avatar-button.svelte';
	import { primaryLinks, secondaryLinks } from '@utils';
	import Icon from '@iconify/svelte';
	const drawerStore = getDrawerStore();
	// const settings = { id: 'example-1' };
	function drawerOpenLeftNavigation(): void {
		drawerStore.open({
			id: 'drawer-side-link-list',
			width: 'w-full max-w-[240px] sm:max-w-[400px]'
		});
	}

	const user = $page.data.user;
</script>

<AppBar
	background="bg-surface-100-800-token"
	padding="p-4"
	shadow="shadow-md"
	slotLead="place-start ml-8"
	slotDefault="place-center"
	slotTrail="place-end mr-8"
>
	<svelte:fragment slot="lead">
		<a href="/">
			<img src="https://storage.daedalus.codes/logo.png" alt="logo" class="h-[50px]" />
		</a>
	</svelte:fragment>
	<div class="flex justify-center">
		<div class="me-auto flex gap-5 lg:gap-10">
			{#each primaryLinks as link}
				{#if link.href !== '/'}
					<a
						href={link.href}
						class="hidden border-y-4
					border-transparent md:flex md:items-center
					{$page.url.pathname === link.href ? 'active' : ''}"
					>
						{link.name}
					</a>
				{/if}
			{/each}
		</div>
		{#if !$page.data.user}
			<div class="flex gap-5 lg:gap-10">
				{#each secondaryLinks as link}
					<a
						href={link.href}
						class="hidden border-y-4
				border-transparent md:flex md:items-center
				{$page.url.pathname === link.href ? 'active' : ''}"
					>
						{link.name}
					</a>
				{/each}
			</div>
		{/if}
	</div>
	<svelte:fragment slot="trail">
		<a href="/search" class="text-2xl">
			<Icon icon="iconamoon:search" />
		</a>

		{#if user}
			<AvatarButton />
		{:else}
			<a
				href="/login"
				data-sveltekit-preload-data="hover"
				class="hidden md:variant-filled-primary md:btn md:flex"
			>
				<Icon icon="material-symbols:login" class="text-2xl" />
				<span class="hidden md:inline-block">Login</span>
			</a>
		{/if}
		<button class="text-2xl md:hidden" on:click={drawerOpenLeftNavigation}>
			<Icon icon="mdi:menu" />
		</button>
		<LightSwitch />
	</svelte:fragment>
</AppBar>
