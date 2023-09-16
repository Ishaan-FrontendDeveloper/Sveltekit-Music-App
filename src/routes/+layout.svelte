<script lang="ts">
  //All the imports and stuff
	import '../app.postcss';
  import {AppShell} from '@skeletonlabs/skeleton'
  import {initializeStores,Drawer,getDrawerStore} from '@skeletonlabs/skeleton'
	// Floating UI for Popups
	import { computePosition, autoUpdate, flip, shift, offset, arrow } from '@floating-ui/dom';
	import { storePopup } from '@skeletonlabs/skeleton';
	storePopup.set({ computePosition, autoUpdate, flip, shift, offset, arrow });
  import Header from './header.svelte'
  import Footer from './footer.svelte'
  import SideBar from './sidebar.svelte'
  </script>
 <AppShell class="gap-3 p-3 " slotSidebarLeft="bg-surface-800/5 w-0 lg:w-72">
	<!-- (header) -->
	<svelte:fragment slot="sidebarLeft">
     <SideBar/> 
  </svelte:fragment>
	<!-- (sidebarRight) -->
	<svelte:fragment slot="pageHeader"><main class="m-2"><Header/></main></svelte:fragment>
	<!-- Router Slot -->
	<slot />
	<!-- ---- / ---- -->
	<svelte:fragment slot="pageFooter"><main class="m-2"><Footer/></main></svelte:fragment>
	<svelte:fragment slot="footer">THE PLAYER WOULD BE HERE</svelte:fragment>

</AppShell>

