<script lang="ts">
  import {AppShell} from '@skeletonlabs/skeleton'
import {initializeStores, getDrawerStore } from "@skeletonlabs/skeleton";
initializeStores();
const drawerStore = getDrawerStore();

function drawerClose(): void {
     drawerStore.close();
}
</script>
<AppShell class="flex flex-col my-2 justify-center items-stretch p-2   content-center text-center rounded-md bg-zinc-900 w-72 ">
	<svelte:fragment slot="pageHeader">
  <a class="flex content-center p-3 gap-3" href='/'>
   <svg class="w-[32px] h-[32px] text-gray-800 dark:text-white" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 18 16">
    <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="1.2" d="M14 11.5V1s3 1 3 4m-7-3H1m9 4H1m4 4H1m13 2.4c0 1.325-1.343 2.4-3 2.4s-3-1.075-3-2.4S9.343 10 11 10s3 1.075 3 2.4Z"/>
  </svg>
  <h2 class="h2">Muse</h2>
 </a>
  </svelte:fragment>
	<!-- Router Slot -->
	<ul class="list">
    <li class='flex  p-3   text-center content-center'>
     <span><svg class="w-[24px] h-[24px] text-gray-800 dark:text-white" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="currentColor" viewBox="0 0 20 20">
    <path d="m19.707 9.293-2-2-7-7a1 1 0 0 0-1.414 0l-7 7-2 2a1 1 0 0 0 1.414 1.414L2 10.414V18a2 2 0 0 0 2 2h3a1 1 0 0 0 1-1v-4a1 1 0 0 1 1-1h2a1 1 0 0 1 1 1v4a1 1 0 0 0 1 1h3a2 2 0 0 0 2-2v-7.586l.293.293a1 1 0 0 0 1.414-1.414Z"/>
  </svg> </span>
    <a href='/' on:click={drawerClose}>Home</a>
    </li>
    <li class="flex p-3 content-center"><span><svg class="w-[24px] h-[24px] text-gray-800 dark:text-white" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="currentColor" viewBox="0 0 20 20">
    <path d="M8 15.5a7.5 7.5 0 1 0 0-15 7.5 7.5 0 0 0 0 15Zm11.707 2.793-4-4a1 1 0 0 0-1.414 1.414l4 4a1 1 0 0 0 1.414-1.414Z"/>
    </svg></span><a href='/search' on:click={drawerClose}>Search</a></li>
    
  </ul>



</AppShell>



