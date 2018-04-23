+++
draft = false
title = "Feedback Form"
description="Feedback form for the working group"
language = "en"
tags = [
    "feedback"
]
date = "2018-03-22T13:10:52-05:00"
type = "single"
+++

<div class="wb-frmvld wb-fdbck nojs-hide mrgn-bttm-lg">
	<p>In order to help the working group please offer some:</p>
	<ul class="mrgn-bttm-lg">
		<li>Session(s) proposals</li>
		<li>Constructive feedback</li>
		<li>Topics you would like to see</li>
	</ul>
	<form action="https://formspree.io/william.hearn@canada.ca" method="post">
		<input type="hidden" name="language" value="en">
		<div id="type">
			<div class="form-group">
				<label for="fbreg" class="required">
					<span class="field-name">Classification</span>
					<strong class="required">(required)</strong>
				</label>
				<select class="form-control" name="fbreg" id="fbreg" required="required">
					<option value="">Select a classification</option>
					<option value="subject1">Governent Employee</option>
					<option value="subject2">Private Sector</option>
					<option value="other">Other</option>
				</select>
			</div>
			<div class="form-group">
				<label for="fbname" class="required">
					<span class="field-name">Name</span>
				</label>
				<input class="form-control" type="text" id="fbname" name="fbname" size="45" maxlength="60">
			</div>
			<div class="form-group">
				<label for="fbemail" class="required">
					<span class="field-name">Email</span>
				</label>
				<input class="form-control" type="email" id="fbemail" name="fbemail" size="45" maxlength="60">
			</div>
			<div class="form-group">
				<label for="fbmsg" class="required">
					<span class="field-name">Message</span>
					<strong class="required">(required)</strong>
				</label>
				<textarea class="form-control" id="fbmsg" name="fbmsg" rows="5" cols="45" required="required"></textarea>
			</div>
		</div>
		<input type="submit" name="fbsbmt" id="fbsbmt" value="Submit feedback" class="btn btn-primary">
		<input type="reset" value="Reset" class="btn btn-default">
	</form>
</div>
