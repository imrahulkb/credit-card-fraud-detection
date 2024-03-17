<script>
  import { onMount } from 'svelte';
  import Navbar from './Navbar.svelte';

  let fileInput;

  // Mimic the file reports data that might be fetched from an API
  let fileReports = [];

  onMount(() => {
    // Simulating fetching file reports on mount
    fetchFileReports();
  });

  function uploadFile() {
    const files = fileInput.files;

    if (files.length === 0) {
      alert('Please select a file to upload.');
      return;
    }

    const formData = new FormData();
    formData.append('file', files[0]);

    // Here you would make an AJAX request to upload the file
    // For demonstration purposes, we'll just log the file data
    console.log('Uploading File:', files[0].name);
  }

  function fetchFileReports() {
    // Simulate fetching file reports
    fileReports = [
      { name: 'Report 1', date: '2024-03-04', status: 'Completed' },
      { name: 'Report 2', date: '2024-03-05', status: 'Processing' },
      { name: 'Report 3', date: '2024-03-06', status: 'Failed' }
    ];
  }
</script>
<style>
  header {
    background-color: #f0f0f0;
    padding: 10px;
    margin-bottom: 20px;
  }

  nav ul {
    list-style-type: none;
    padding: 0;
  }

  nav ul li {
    display: inline;
    margin-right: 20px;
  }

  .dashboard-section {
    margin-bottom: 30px;
  }

  .dashboard-section h2 {
    border-bottom: 1px solid #ccc;
    padding-bottom: 5px;
  }
</style>

<header>
  <h1>Welcome to Your Dashboard</h1>
  <nav>
    <ul>
      <li><a href="#upload">Upload Files</a></li>
      <li><a href="#reports">View Reports</a></li>
      <li><a href="#account">My Account</a></li>
    </ul>
  </nav>
</header>

<section id="upload" class="dashboard-section">
  <h2>Upload Files</h2>
  <input type="file" bind:this={fileInput}>
  <button on:click={uploadFile}>Upload</button>
</section>

<section id="reports" class="dashboard-section">
  <h2>File Reports</h2>
  <div id="fileReports">
    {#each fileReports as report}
      <div class="file-report">
        <strong>{report.name}</strong> - {report.date} ({report.status})
      </div>
    {/each}
  </div>
</section>

<section id="account" class="dashboard-section">
  <h2>My Account</h2>
  <p>Name: John Doe</p>
  <p>Email: johndoe@example.com</p>
</section>
