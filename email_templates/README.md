EmailJS booking template (Vietnamese)

Files:
- booking_template_emailjs.html: HTML email template ready to paste into EmailJS.

How to use in EmailJS:
1. Sign in to EmailJS and go to "Email Templates" -> "Create New Template".
2. Choose the HTML editor and paste the contents of booking_template_emailjs.html.
3. Use the following template variable names in the template (they are already included):
   - {{to_email}} (recipient)
   - {{booking_ref}}
   - {{name}}
   - {{package_type}}
   - {{date}}
   - {{adults}}
   - {{students}}
   - {{special_requirements}}
4. Save the template and copy the Template ID.
5. In `d:\bmgt\index.html`, replace the placeholders in the `sendEmailNotification` call if necessary:
   - service_id: your EmailJS service id (e.g., service_xxx)
   - template_id: the Template ID from EmailJS
   - user_id: your EmailJS public key / user id

Notes & tips:
- EmailJS public key (user id) is intended to be used from client-side code but treat any server-side secret keys carefully.
- Test sending from the EmailJS template editor first to validate layout and variables.
- If you want a plain-text alternative, add a text-only section in EmailJS using the editor's plain text option or keep the current HTML which has readable content for most email clients.
