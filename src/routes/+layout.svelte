<script>
  import Footer from '$lib/components/Footer/Footer.svelte';
  import Navbar from '$lib/components/Navbar/Navbar.svelte';
  import Shell from '$lib/components/Shell/Shell.svelte';
  import '../app.css';
</script>

<Shell>
  <svelte:fragment slot="header">
    <Navbar />
  </svelte:fragment>
  <!-- <svelte:fragment slot="sidebarLeft">sidebarLeft</svelte:fragment>
  <svelte:fragment slot="pageHeader">pageHeader</svelte:fragment> -->

  <slot />

  <!-- <svelte:fragment slot="pageFooter">pageFooter</svelte:fragment>
  <svelte:fragment slot="sidebarRight">sidebarRight</svelte:fragment> -->
  <svelte:fragment slot="footer">
    <Footer />
  </svelte:fragment>
</Shell>
