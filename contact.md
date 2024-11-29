---
layout: default
title: Contact
---

# Contact Me

Have a question or want to collaborate? Feel free to get in touch by filling out the form below. I’ll get back to you as soon as possible.

---

<form id="contact-form">
  <div class="form-group">
    <label for="name">Name:</label>
    <input type="text" id="name" name="name" placeholder="Your Name" required>
  </div>
  
  <div class="form-group">
    <label for="email">Email:</label>
    <input type="email" id="email" name="email" placeholder="Your Email" required>
  </div>
  
  <div class="form-group">
    <label for="subject">Subject:</label>
    <input type="text" id="subject" name="subject" placeholder="Subject" required>
  </div>
  
  <div class="form-group">
    <label for="message">Message:</label>
    <textarea id="message" name="message" placeholder="Your Message" rows="5" required></textarea>
  </div>
  
  <button type="submit">Send Message</button>
</form>

<div id="confirmation-message" class="hidden">
  <p>Thank you! Your message has been sent successfully. I will get back to you soon.</p>
</div>

---

<script>
  document.getElementById('contact-form').addEventListener('submit', function(event) {
    event.preventDefault(); // Prevent form submission

    // Simple Form Validation
    const name = document.getElementById('name').value.trim();
    const email = document.getElementById('email').value.trim();
    const subject = document.getElementById('subject').value.trim();
    const message = document.getElementById('message').value.trim();
    const confirmation = document.getElementById('confirmation-message');

    if (!name || !email || !subject || !message) {
      alert('Please fill in all fields.');
      return;
    }

    // Validate Email Format
    const emailPattern = /^[^@\s]+@[^@\s]+\.[^@\s]+$/;
    if (!emailPattern.test(email)) {
      alert('Please enter a valid email address.');
      return;
    }

    // Simulate successful submission
    confirmation.classList.remove('hidden');
    confirmation.scrollIntoView({ behavior: 'smooth' });

    // Clear the form fields
    document.getElementById('contact-form').reset();
  });
</script>

<style>
  .hidden {
    display: none;
  }

  .form-group {
    margin-bottom: 1em;
  }

  label {
    display: block;
    font-weight: bold;
    margin-bottom: 0.5em;
  }

  input, textarea, button {
    width: 100%;
    padding: 0.8em;
    margin-bottom: 0.5em;
    border: 1px solid #ccc;
    border-radius: 5px;
  }

  button {
    background-color: #007BFF;
    color: white;
    border: none;
    cursor: pointer;
  }

  button:hover {
    background-color: #0056b3;
  }

  #confirmation-message {
    margin-top: 1.5em;
    padding: 1em;
    background-color: #d4edda;
    color: #155724;
    border: 1px solid #c3e6cb;
    border-radius: 5px;
  }
</style>
