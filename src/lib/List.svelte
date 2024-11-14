<script lang="ts">
   let list = [...Array(8)].map((_, i) => i)
   let selected: number = $state(0)

   const selectMe = (index: number) => {
      selected = index
   }
</script>

<div>
   {#each list as n, i (n)}
      <button onclick={() => selectMe(i)}>{i}</button>
   {/each}
</div>
