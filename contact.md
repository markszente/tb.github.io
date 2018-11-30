---
layout: default
title: Contact - Team Brookvale
permalink: /contact
---
<script type="text/javascript">
    function sendEmail() {
        var service_id = 'gmail-longbtomi';
        var template_id = 'contact_form';
        var form = document.forms['contactForm'];
        var templateParams = {
            name: form["name"].value,
            from_email: form["from_email"].value,
            phone: form["phone"].value,
            subject: form["subject"].value,
            message: form["message"].value
        };
  
        emailjs.send(service_id, template_id, templateParams)
            .then(function(response) {
                console.log('Message sent');
            }, function(error) {
                console.log('Failed to send message');
            });
    }
</script>
<div class="contactpage">
    <div class="pagehero">
        <div class="inner flex sb">
            <div>
                <h1>Contact</h1>
                <p style="margin-bottom: 50px">We develop software products and provide digital platform engineering services on the Northern Beaches of Sydney</p>
                <img src="/assets/images/arrowdown.png">
            </div>
            <div class="pageheropic jumptop">
                &nbsp;
            </div>
        </div>
    </div>
    <div class="inner flex sb">
        <div style="width: 659px">
            <h2>Make people interact with each other, that’s what Internet is all about and that’s what this website is about too.</h2>
            <div class="mid gray">
                Glad to see you anytime from 10am to 6pm except on Saturday, Sunday and official vacations. 
            </div>
            <div class="contact semibold" style="margin: 30px 0 40px 0">
                <div class="floleft" style="width: 150px">Phone:</div><div class="bluetext">{{ site.data.text.footer.phone }}</div>
                <div class="floleft" style="width: 150px">Email:</div><div class="bluetext">{{ site.data.text.footer.email }}</div>
            </div>
            <a href="https://www.facebook.com/teambrookvale/" class="floleft blueback fb"><img src="/assets/images/facebook.svg"></a>
        </div>
        <div style="width: 460px">
            <form id="contactForm" style="margin-bottom: 80px">
                <div class="row">
                    <label>Name</label>
                    <input type="text" name="name" placeholder="Name">
                </div>
                <div class="flex sb">
                    <div style="width: 48%">
                        <div class="row">
                            <label>Email</label>
                            <input type="email" name="from_email" placeholder="Email">
                        </div>
                    </div>
                    <div style="width: 48%">
                        <div class="row">
                            <label>Phone number</label>
                            <input type="text" name="phone" placeholder="Phone number">
                        </div>
                    </div>
                </div>
                <div class="row">
                    <label>Subject</label>
                    <select name="subject" placeholder="Name"><option>Please select</option></select>
                </div>
                <div class="row">
                    <label>Message</label>
                    <textarea name="message" placeholder="Your message here..."></textarea>
                </div>
                <div class="row buttons">
                    <button type="button" onclick="sendEmail()">Send message</button>
                </div>
            </form>
        </div>
    </div>
</div>