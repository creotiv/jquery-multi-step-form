======================
Jquery multi step form
======================

Multi step form with progress bar for jquery

Example of use 
==============

Add three lines to the HEAD:

::

    <script src="http://thecodeplayer.com/uploads/js/jquery-1.9.1.min.js" type="text/javascript"></script>
    <script src="http://thecodeplayer.com/uploads/js/jquery.easing.min.js" type="text/javascript"></script>
    <script src="jquery-multi-step-form.js" type="text/javascript"></script>
    <link href="jquery-multi-step-form.css" media="screen" rel="stylesheet" type="text/css"/>


Add this to page code:

::

    <div id="multistepform-example-container" style="display:none;">
        <ul id="multistepform-progressbar">
            <li class="active">Account Setup</li>
            <li>Social Profiles</li>
            <li>Personal Details</li>
        </ul>
        <div class="form">
            <form action="">
            <h2 class="fs-title">Create your account</h2>
            <h3 class="fs-subtitle">This is step 1</h3>
            <input type="text" name="email" placeholder="Email">
            <input type="password" name="pass" placeholder="Password">
            <input type="password" name="cpass" placeholder="Confirm Password">
            <input type="button" name="next" class="next button" value="Next">
            </form>
        </div>
        <div class="form">
            <form action="">
            <h2 class="fs-title">Social Profiles</h2>
            <h3 class="fs-subtitle">Your presence on the social network</h3>
            <input type="text" name="twitter" placeholder="Twitter">
            <input type="text" name="facebook" placeholder="Facebook">
            <input type="text" name="gplus" placeholder="Google Plus">
            <input type="button" name="previous" class="previous button" value="Previous">
            <input type="button" name="next" class="next button" value="Next">
            </form>
        </div>
        <div class="form">
            <form action="">
            <h2 class="fs-title">Personal Details</h2>
            <h3 class="fs-subtitle">We will never sell it</h3>
            <input type="text" name="fname" placeholder="First Name">
            <input type="text" name="lname" placeholder="Last Name">
            <input type="text" name="phone" placeholder="Phone">
            <textarea name="address" placeholder="Address"></textarea>
            <input type="button" name="previous" class="previous button" value="Previous">
            <input type="button" name="submit" class="next button" value="Finish">
            </form>
        </div>
    </div>

    <div>
      <p><a href="javascript:void()" class="open-form">Click to open example form</a></p>
    </div>

    <script>
        $(document).ready(function(){
            $('.open-form').click(function(){
                $.multistepform({
                    container:'multistepform-example-container',
                    form_method:'GET',
                })
            });
        });
    </script>
