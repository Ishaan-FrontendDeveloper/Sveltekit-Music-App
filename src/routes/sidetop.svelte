<script lang="ts">
  import {AppShell} from '@skeletonlabs/skeleton'
</script>
<AppShell class="flex flex-col w-64 m-2  p-3 gap-3 text-center rounded-md bg-zinc-900  ">
	<svelte:fragment slot="pageHeader">
  <div class="flex content-center gap-2">
   <svg class="w-[24px] h-[24px] text-gray-800 dark:text-white" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 18 16">
    <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="1.2" d="M14 11.5V1s3 1 3 4m-7-3H1m9 4H1m4 4H1m13 2.4c0 1.325-1.343 2.4-3 2.4s-3-1.075-3-2.4S9.343 10 11 10s3 1.075 3 2.4Z"/>
  </svg>
  <h3 class="h3"> Muse</h3>
 </div>
  </svelte:fragment>
	<!-- Router Slot -->
	<ul class="list">
    <li class='flex content-center'>
      <svg class="w-[20px] h-[20px] m-2 text-gray-800 dark:text-white" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 20 20">
    <path stroke="currentColor" strokeLinecap="round" strokeLinejoin="round" strokeWidth="1.2" d="M3 8v10a1 1 0 0 0 1 1h4v-5a1 1 0 0 1 1-1h2a1 1 0 0 1 1 1v5h4a1 1 0 0 0 1-1V8M1 10l9-9 9 9"/>
  </svg>
    Home
    </li>
    <li><svg class="w-[20x] h-[20px] text-gray-800 dark:text-white" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 20 20">
    <path stroke="currentColor" strokeLinecap="round" strokeLinejoin="round" strokeWidth="1.2" d="m19 19-4-4m0-7A7 7 0 1 1 1 8a7 7 0 0 1 14 0Z"/>
  </svg>Search</li>
  </ul>



</AppShell>



