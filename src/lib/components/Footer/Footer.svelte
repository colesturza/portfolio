<script lang="ts">
  let currentYear = new Date().getFullYear();
</script>

<div class="bg-slate-900">
  <div class="max-w-7xl mx-auto px-8">
    <!-- prettier-ignore -->
    <div class="flex justify-between">
      <p class="text-slate-100 text-sm py-3 px-3">
        Copyright &copy; {currentYear} Cole Sturza. Powered by 
        <a class="hover:text-purple-500" href="https://svelte.dev/" target="_blank" rel="noopener noreferrer">Svelte</a>
        and <a class="hover:text-purple-500" href="https://tailwindcss.com/" target="_blank" rel="noopener noreferrer">Tailwind CSS</a>.
      </p>
      <div class="flex items-center space-x-1">
        <a class="py-3 px-3 text-slate-100 hover:text-purple-500" href="https://github.com/colesturza"><i class="fa-brands fa-github"></i></a>
        <a class="py-3 px-3 text-slate-100 hover:text-purple-500" href="https://gitlab.com/colesturza1"><i class="fa-brands fa-gitlab"></i></a>
        <a class="py-3 px-3 text-slate-100 hover:text-purple-500" href="https://www.linkedin.com/in/cole-sturza/"><i class="fa-brands fa-linkedin"></i></a>
        <a class="py-3 px-3 text-slate-100 hover:text-purple-500" href="mailto:colesturza@gmail.com"><i class="fa-solid fa-paper-plane"></i></a>
      </div>
    </div>
  </div>
</div>
