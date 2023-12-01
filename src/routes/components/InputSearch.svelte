<script>
  import { Search } from 'flowbite-svelte';
  let searchTerm = '';
</script>

<style>
  .search-container {
    position: relative;
    display: flex;
    align-items: center;
  }

  .search-icon {
    position: absolute;
    left: 10px; 
    width: 14px; 
    height: 16px; 
    fill: #666; 
  }

  .search-input {
    padding-left: 30px;
    width: 145px; 
    height: 24px; 
    border: 1px solid #ccc; 
  }
</style>

<form class="relative">
  <label class="search-container">
    <svg class="search-icon" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 16 16">
      <path d="M12.293 11.293l3.714 3.714a1 1 0 01-1.414 1.414l-3.714-3.714a7 7 0 111.414-1.414zM7 13a6 6 0 100-12 6 6 0 000 12z"/>
    </svg>
    <input type="text" bind:value={searchTerm} placeholder="Pesquisar" class="search-input p-2" />
  </label>
</form>