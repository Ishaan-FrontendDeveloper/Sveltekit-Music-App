<script lang="ts">
  import {AppBar} from '@skeletonlabs/skeleton'
</script>

<div>
<AppBar class="p-3 m-2 text-center rounded-md bg-gradient-to-b  from-zinc-900  to-transparent " gridColumns="grid-cols-3" slotDefault="place-self-center" slotTrail="place-content-end">

	<svelte:fragment slot="lead"><div class="">i</div></svelte:fragment>
    Heade
	<svelte:fragment slot="trail">
      <div class='flex gap-3 text-gray-400 '>
      <ul class="flex content-center gap-3 ">
        <li>
          Support
        </li>
        <li>
          Download
        </li>
      </ul>
      <div class="border-l-2 border-grey-500"></div>
      <ul class="flex p-r-3 gap-5">
        <li class="">
         <a href='/sign' >Sign up</a>
        </li>
        <li class="">
         <a class="" href ='/log'>  Log in </a>
        </li>
      </ul>
      </div>
    </svelte:fragment>
</AppBar>
</div>
