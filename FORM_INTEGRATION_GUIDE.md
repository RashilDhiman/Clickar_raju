# Contact Form Integration Guide

## ✅ Current Setup: FormSubmit (Active)

Your contact form is now integrated with **FormSubmit** - a free service that sends form submissions directly to your email.

### How It Works

1. **When someone fills out the form** and clicks "Request Quote"
2. **FormSubmit receives the submission** and formats it nicely
3. **You receive an email** at `rajatjais927@gmail.com` with all the form data
4. **User sees a success message** confirming their submission

### What You'll Receive

Each form submission will include:
- **Name/Company Name**
- **Email Address**
- **Phone Number**
- **Service Type** (Product Photography, Image Editing, etc.)
- **Project Requirements/Message**

### Email Format

You'll receive emails with the subject: **"New Quote Request - Clickkar Raju"**

The email will contain all form fields in a nicely formatted box template.

### No Setup Required!

FormSubmit works immediately - no signup, no API keys, no configuration needed. Just make sure your email address is correct in the form action.

---

## 🔧 Alternative: EmailJS (More Features)

If you want more control and features, you can use EmailJS instead. Here's how:

### Step 1: Sign up for EmailJS (Free)
1. Go to https://www.emailjs.com/
2. Sign up for a free account
3. Create a new email service (Gmail, Outlook, etc.)
4. Create an email template

### Step 2: Get Your Credentials
- **Service ID**: From your email service
- **Template ID**: From your email template
- **Public Key**: From your account settings

### Step 3: Update the Code

Replace the form action in `index.html`:
```html
<!-- Remove the FormSubmit action -->
<form id="contactForm">
```

Add EmailJS script before closing `</body>` tag:
```html
<script src="https://cdn.jsdelivr.net/npm/@emailjs/browser@3/dist/email.min.js"></script>
<script>
    emailjs.init("YOUR_PUBLIC_KEY");
</script>
```

Update `script.js` contact form handler:
```javascript
contactForm.addEventListener('submit', (e) => {
    e.preventDefault();
    
    emailjs.sendForm('YOUR_SERVICE_ID', 'YOUR_TEMPLATE_ID', contactForm)
        .then(() => {
            formMessage.textContent = 'Thank you! Your message has been sent successfully.';
            formMessage.className = 'form-message success';
            contactForm.reset();
        }, (error) => {
            formMessage.textContent = 'Something went wrong. Please try again.';
            formMessage.className = 'form-message error';
        });
});
```

---

## 📧 Testing Your Form

1. **Fill out the form** on your website
2. **Submit it**
3. **Check your email** (rajatjais927@gmail.com)
4. You should receive the form submission

### Note:
- First submission from a new domain/IP might take 1-2 minutes
- Check spam folder if you don't see it
- FormSubmit free tier: 50 submissions/month

---

## 🎯 Customization Options

### Change Email Subject
Edit in `index.html`:
```html
<input type="hidden" name="_subject" value="Your Custom Subject">
```

### Add Redirect After Submission
Edit in `index.html`:
```html
<input type="hidden" name="_next" value="https://yourwebsite.com/thank-you">
```

### Enable Honeypot (Spam Protection)
Add to form:
```html
<input type="text" name="_honey" style="display:none">
```

---

## ❓ Troubleshooting

**Form not sending?**
- Check internet connection
- Verify email address is correct
- Check browser console for errors
- Try submitting from a different browser

**Not receiving emails?**
- Check spam/junk folder
- Verify email address in form action
- Wait 1-2 minutes (first submission delay)
- Try a test submission

**Need more submissions?**
- FormSubmit free: 50/month
- Upgrade to paid plan for more
- Or switch to EmailJS (free tier: 200/month)

---

## 📞 Support

- FormSubmit: https://formsubmit.co/
- EmailJS: https://www.emailjs.com/docs/

---

**Your form is ready to use!** Just upload your website and start receiving form submissions. 🎉

