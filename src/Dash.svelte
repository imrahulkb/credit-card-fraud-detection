<!-- Home.svelte -->
<script>
  import UploadCreditData from "./Upload_credit_data.svelte";

  const routes = {
      UploadCreditData: "/Upload_credit_data", 
      reports: "/reports",
      account_details: "/account_details",
  };

  // Function to handle navigation (replace with Svelte routing)
  function navigateTo(route) {
      window.location.href = route; 
  }
</script>



<main id="main">

  <!-- ======= Hero Section ======= -->
  <section id="homesection" style="padding: 0px 0px;">
    <!--__________________________________ header-box______________________________________________ -->
    <div id="header-container">
      <h1 id="header2">USER DASHBOARD</h1>
    </div>
    <!-- ___________________________________main-division____________________________________________ -->
    <div id="main-container">
      <div class="inner-box">
        <button on:click={() => navigateTo(routes.UploadCreditData)}>
          <svg viewBox="0 0 80 80" width="200px" height="200px">
            <circle class="circle" cx="40" cy="40" r="38"/>
            <text x="40" y="35" font-size="10px" fill="#FFFFFF" text-anchor="middle">Upload</text>
            <text x="40" y="47" font-size="10px" fill="#FFFFFF" text-anchor="middle">Files</text>
          </svg>
        </button>
      </div>

      <div class="inner-box">
        <button on:click={() => navigateTo(routes.reports)}>
          <svg viewBox="0 0 80 80" width="200px" height="200px">
            <circle class="circle" cx="40" cy="40" r="38"/>
            <text x="40" y="35" font-size="10px" fill="#FFFFFF" text-anchor="middle">Files</text>
            <text x="40" y="47" font-size="10px" fill="#FFFFFF" text-anchor="middle">Report</text>
          </svg>
        </button>
      </div>

      <div class="inner-box">
        <button on:click={() => navigateTo(routes.account_details)}>
          <svg viewBox="0 0 80 80" width="200px" height="200px">
            <circle class="circle" cx="40" cy="40" r="38"/>
            <text x="40" y="35" font-size="10px" fill="#FFFFFF" text-anchor="middle">My</text>
            <text x="40" y="47" font-size="10px" fill="#FFFFFF" text-anchor="middle">Account</text>
          </svg>
        </button>
      </div>
    </div>
  </section><!-- End Hero -->
</main>

