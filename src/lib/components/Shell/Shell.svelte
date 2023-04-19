<script lang="ts">
  /**
   * @slot header
   * @slot sidebarLeft
   * @slot sidebarRight
   * @slot pageHeader
   * @slot pageFooter
   * @slot footer
   */
</script>

<div class="w-screen h-screen flex flex-col overflow-hidden">
  
  {#if $$slots.header}
    <header class="flex-none z-10"><slot name="header" /></header>
  {/if}

  <div class="w-full h-full flex flex-auto overflow-hidden">
    
    {#if $$slots.sidebarLeft}
      <aside class="flex-none overflow-x-hidden overflow-y-auto w-auto"><slot name="sidebarLeft" /></aside>
    {/if}

    <div class="flex flex-1 flex-col overflow-x-hidden">

      {#if $$slots.pageHeader}
        <header class="flex-none"><slot name="pageHeader" /></header>
      {/if}

      <main class="flex flex-1 flex-col overflow-x-hidden"><slot /></main>

      {#if $$slots.pageFooter}
        <footer class="flex-none"><slot name="pageFooter" /></footer>
      {/if}
    
    </div>

    {#if $$slots.sidebarRight}
      <aside class="flex-none overflow-x-hidden overflow-y-auto w-auto"><slot name="sidebarRight" /></aside>
    {/if}

  </div>

  {#if $$slots.footer}
    <footer class="flex-none z-10"><slot name="footer" /></footer>
  {/if}

</div>
