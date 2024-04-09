<!-- Home.svelte -->
<script>
  import { onMount } from 'svelte';
  // Assuming you have routing logic here
  const urls = {
      upload_data: "/Upload_credit_data" // Replace with your actual URL
  };
</script>

<main id="main">

  <!-- ======= Hero Section ======= -->
  <section id="homesection" style="padding: 0px 0px;">
      <!--__________________________________ header-box______________________________________________ -->
      <div id="header-container" style="margin-bottom: 20px;">
          <h1 id="header2" style="font-size: 24px;">Upload Credit Data Files</h1>
      </div>
      <!-- ___________________________________main-division____________________________________________ -->
      <div id="upload-container">
          <div id="upload-header-container" style="margin-bottom: 10px;">
              <h3 id="upload-header" style="font-size: 18px;">UPLOAD CREDIT CARD DATASET</h3>
          </div>
          <div class="upload">
              <form class="upload-form" action="{urls.upload_data}" method="post" enctype="multipart/form-data">
                  <!-- CSRF token -->
                  <!-- svelte-ignore missing-declaration -->
                  <input type="hidden" name="csrf_token" value="{{ csrf_token }}">
                  <label for="filename" style="font-weight: bold;">File Name</label><br>
                  <input type="text" name="data_file_name" id="filename" style="margin-bottom: 10px; padding: 5px;" placeholder="File Name"><br>
                  <!-- svelte-ignore a11y-label-has-associated-control -->
                  <label style="font-weight: bold;">Upload Credit Card Dataset File</label><br>
                  <input id="file" type="file" name="actual_file_name" style="margin-bottom: 10px;"><br>
                  <label for="description" style="font-weight: bold;">Description of the File</label><br>
                  <textarea placeholder="Description" name="description" id="description" style="margin-bottom: 10px; padding: 5px;"></textarea><br>
                  <input id="btn" type="submit" value="SUBMIT" style="background-color: #007bff; color: #fff; padding: 8px 16px; border: none; border-radius: 4px; cursor: pointer;">
              </form>
          </div>
      </div>
  </section><!-- End Hero -->

</main>

<style>
  /* Your CSS styles go here */
  /* You can use inline styles or import CSS files directly */
</style>
