<script lang="ts">
	import '../app.postcss';
  import {AppShell} from '@skeletonlabs/skeleton'
	// Floating UI for Popups
	import { computePosition, autoUpdate, flip, shift, offset, arrow } from '@floating-ui/dom';
	import { storePopup } from '@skeletonlabs/skeleton';
	storePopup.set({ computePosition, autoUpdate, flip, shift, offset, arrow });
  import Header from './header.svelte'
  import Footer from './footer.svelte'
  import SideBar from './sidebar.svelte'
</script>
 
<AppShell class="gap-3 p-3">
	<!-- (header) -->
	<svelte:fragment slot="sidebarLeft">
     <SideBar/> 
  </svelte:fragment>
	<!-- (sidebarRight) -->
	<svelte:fragment slot="pageHeader"><Header/></svelte:fragment>
	<!-- Router Slot -->
	<slot />
	<!-- ---- / ---- -->
	<svelte:fragment slot="pageFooter"><Footer/></svelte:fragment>
	<svelte:fragment slot="footer">falana</svelte:fragment>

</AppShell>

