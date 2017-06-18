---
layout: page
title: Contact
permalink: /contact/
---

# Email Us
Have questions you would like a Canberra GPN tutor to answer? Interested in becoming a tutor yourself? Noticed a problem with the website? We’d love to hear from you!

Send us an email at [canberragpn@gmail.com](mailto:canberragpn@gmail.com)!

# Sign Up to GPN Announcements
<form action="https://docs.google.com/forms/d/e/1FAIpQLSeyEVeUQ1NXcs5vkkG6hqBat6NbAMz1VFh6ASTPie-uNt3DgA/formResponse" method="post">
<div class="form-group row">
  <label for="subscribe-fname" class="col-sm-2 col-form-label">First Name</label>
  <div class="col-sm-5">
    <input type="text" class="form-control" id="subscribe-fname" name="entry.915194881" aria-describedby="subscribe-fname-error">
  </div>
</div>
<div class="form-group row">
  <label for="subscribe-lname" class="col-sm-2 col-form-label">Last Name</label>
  <div class="col-sm-5">
    <input type="text" class="form-control" id="subscribe-lname" name="entry.887862633" aria-describedby="subscribe-lname-error">
  </div>
</div>
<div class="form-group row">
  <label for="subscribe-email" class="col-sm-2 col-form-label">Email address</label>
  <div class="col-sm-10">
    <input type="text" class="form-control" id="subscribe-email" name="entry.743158204" aria-describedby="subscribe-email-error">
  </div>
</div>
<button type="submit" class="btn btn-default" id="subscribe-form-submit">Sign me up!</button>
</form>
<br>

<div id="subscribe-status" style="display: none;" class="alert" role="alert">
nope
</div>

<script>
$( document ).ready(function() {
	$('#subscribe-form-submit').click(function(e) {
	    e.preventDefault();
	    var contactFirstName = $('#subscribe-fname').val();
	    var contactLastName  = $('#subscribe-lname').val();
	    var contactEmailAddress = $('#subscribe-email').val();
	    // data validation code here
	    var url = "https://docs.google.com/forms/d/e/1FAIpQLSeyEVeUQ1NXcs5vkkG6hqBat6NbAMz1VFh6ASTPie-uNt3DgA/formResponse";
	    var data = {
	        'entry.915194881': contactFirstName,
	        'entry.887862633': contactLastName,
	        'entry.743158204': contactEmailAddress,
	    };
	    $.ajax({
	            type: "POST",
	            url: url,
	            dataType: "json",
	            data: data,
	    }).always(function() {
            $('#subscribe-status').addClass('alert-success');
            $('#subscribe-status').html("<strong>Thanks for signing up to our announcments!</strong>");
            $("#subscribe-status").show();
		});
	});
});
</script>