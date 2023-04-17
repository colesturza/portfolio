<script>
  import Footer from '$lib/components/Footer/Footer.svelte';
  import '../app.css';
  import Navbar from '../lib/components/Navbar/Navbar.svelte';
</script>

<Navbar />

<slot />

<div class="fixed inset-x-0 bottom-0">
  <Footer />
</div>
