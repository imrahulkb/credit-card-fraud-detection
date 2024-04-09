<!-- AllCreditCardDataset.svelte -->
<script>
  import '@fontsource/montserrat'
  import '@fontsource/mulish'
  import Navbar from './Navbar.svelte';
  // Assuming you have all_files data passed to this component
  export let all_files = [];

  // Function to truncate description
  function truncateDescription(description) {
      return description.length > 60 ? `${description.substring(0, 60)}...` : description;
  }
</script>

<main id="main">
<!-- ======= Hero Section ======= -->
<section id="homesection" style="padding: 0px 0px">
  <!--__________________________________ header-box______________________________________________ -->
  <div id="header-container">
    <h1 id="header2">ALL CREDIT CARD DATASET</h1>
  </div>
  <table
    id="example"
    class="table table-striped"
    style="width: 90%; margin: 1% 4%"
  >
    <thead style="background-color: brown; text-align: center">
      <tr>
        <th>Sr. No</th>
        <th>File name</th>
        <th>Description</th>
        <th>Action</th>
      </tr>
    </thead>
    <tbody style="text-align: center">
      {#each all_files as file, index}
      <tr>
        <td>{index + 1}</td>
        <td>{file.file_name}</td>
        <td>{truncateDescription(file.description)}</td>
        <td>
          <a href="{`/view_data/${file.id}`}">
            <button type="button" class="btn btn-primary">
              View Data
            </button>
          </a>
          <a href="{`/delete_data/${file.id}`}">
            <button type="button" class="btn btn-secondary">
              Delete
            </button>
          </a>
          <a href="{`/prediction_button/${file.id}`}">
            <button type="button" class="btn btn-success">
              Prediction
            </button>
          </a>
          <a href="{`/analysis/${file.id}`}">
            <button type="button" class="btn btn-danger">Analysis</button>
          </a>
        </td>
      </tr>
      {/each}
    </tbody>
  </table>
</section>
<!-- End Hero -->
</main>
