---
title: "Star Gram Online Donation Form"
---

<div id="CustomDonationsForm"></div>

<script>
  var LoadCDScripts = function () {
    var cdscript = document.createElement('script');
    cdscript.onerror = function (e) {
        document.head.removeChild(this);
        setTimeout(LoadCDScripts, 1750);
    };
    cdscript.onload = function () {
        CustomDonations.BuildForm({
        account: 'e22f1a89-f7ab-425a-afc4-c74166e6d4da',
        form: 'ef1c78fc-b189-4bb8-ba69-5ff09ad93d83',
        allocation: null, /* optional. Use an allocation ID, like 'AH664' (w/ quotes) to be default selected on form load */
        memberId: null, /* optional. If the current user is authenticated, you can insert their user ID, like '02943' (with quotes) */
        apiVersion: 'v1',
        interval: null, /* if null, then user must select one time or recurring (if enabled). Optionally can set to 'once', 'monthly','quarterly', or 'yearly' */
        loadingText: 'Loading Secure Form...',
        paymentVersion: 2, /*  1: for modal payment window. 2: for inline payment with Google/Apple Pay options */
        baseUrl: 'https://api.customdonations.com',
        mode: 'live', /* change to 'test' to run in test mode. Use card 4242 4242 4242 4242 for testing. */
      });
    };
    cdscript.src = "https://api.customdonations.com/v1/js/form-builder.min.js?v=" + new Date().getTime();
    document.head.appendChild(cdscript);
  }
  LoadCDScripts();
</script>
