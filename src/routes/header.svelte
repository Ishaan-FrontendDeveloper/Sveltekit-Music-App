<script lang="ts">
  import SideTop from './sidetop.svelte'
  import SideMid from './sidemid.svelte'
  import Footer from './footer.svelte'
  import {AppBar} from '@skeletonlabs/skeleton'


  import {initializeStores,Drawer,getDrawerStore} from '@skeletonlabs/skeleton'
//Setting up Drawer
  initializeStores();
  const DrawerStore = getDrawerStore();
  export const drawerOpen = (()=>{
  DrawerStore.open({})

  })
function drawerClose(): void {
     DrawerStore.close();
}

</script>
<Drawer>
  <ul class="flex flex-col p-3 gap-3">
  <li class="flex gap-3"><button on:click={drawerClose}><SideTop/></button><Footer/></li>
  <li><SideMid/></li>
  </ul>
</Drawer>

<div class="">
<AppBar class=" text-center rounded-md text-xs bg-gradient-to-b  from-zinc-900  to-transparent " gridColumns="grid-cols-3" slotDefault="place-self-center" slotTrail="place-content-end">

	<svelte:fragment slot="lead"><div class="flex gap-3">
       <button class="lg:hidden btn btn-sm mr-4" on:click={drawerOpen}>
            <span>
                <svg class="w-[32px] h-[32px] text-gray-800 dark:text-white" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 18 16">
    <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="1.2" d="M14 11.5V1s3 1 3 4m-7-3H1m9 4H1m4 4H1m13 2.4c0 1.325-1.343 2.4-3 2.4s-3-1.075-3-2.4S9.343 10 11 10s3 1.075 3 2.4Z"/>
  </svg>
            </span>
        </button>
        <button>
        <svg class="w-4 h-4 text-gray-800 dark:text-white" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 8 14">
    <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M7 1 1.3 6.326a.91.91 0 0 0 0 1.348L7 13"/>
  </svg>
        </button>
        <button>
<svg class="w-4 h-4 text-gray-800 dark:text-white" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 8 14">
    <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="m1 13 5.7-5.326a.909.909 0 0 0 0-1.348L1 1"/>
  </svg>
        </button>
    </div></svelte:fragment>

	<svelte:fragment slot="trail">
      <div class='flex gap-3 text-gray-400 lg:text-center '>
      <ul class="flex content-center gap-3 ">
        <li>
          Support
        </li>
     </ul>
      <div class="border-l-2 border-grey-500"></div>
      <ul class="flex p-r-3 gap-5">
        
        <li class="">
         <a class="" href ='/log'>  Log in </a>
        </li>
        
      </ul>
      </div>
    </svelte:fragment>
</AppBar>
</div>
