<template>
  <div id="contact">
    <!-- Contact Start -->
    <section class="py-5 wow fadeInUp" data-wow-delay="0.1s" id="contact">
      <h1 class="title pb-3 mb-5">Contact Me</h1>
      <p class="mb-4">
        The contact form is currently inactive. Get a functional and working
        contact form with Ajax & PHP in a few minutes. Just copy and paste the
        files, add a little code and you're done.
        <a href="https://htmlcodex.com/contact-form">Download Now</a>
      </p>
      <form ref="form" @submit.prevent="sendEmail">
        <div class="row g-3">
          <div class="col-md-6">
            <div class="form-floating">
              <input
                type="text"
                name="sender"
                class="form-control border-0 bg-secondary"
                id="name"
                placeholder="Your Name"
              />
              <label for="name">Your Name</label>
            </div>
          </div>
          <div class="col-md-6">
            <div class="form-floating">
              <input
                type="email"
                name="email"
                class="form-control border-0 bg-secondary"
                id="email"
                placeholder="Your Email"
              />
              <label for="email">Your Email</label>
            </div>
          </div>
          <div class="col-12">
            <div class="form-floating">
              <input
                type="text"
                name="subject"
                class="form-control border-0 bg-secondary"
                id="subject"
                placeholder="Subject"
              />
              <label for="subject">Subject</label>
            </div>
          </div>
          <div class="col-12">
            <div class="form-floating">
              <textarea
                class="form-control border-0 bg-secondary"
                name="message"
                placeholder="Leave a message here"
                id="message"
                style="height: 200px"
              ></textarea>
              <label for="message">Message</label>
            </div>
          </div>
          <div class="col-12">
            <button class="btn btn-primary w-100 py-3" type="submit">
              Send Message
            </button>
          </div>
        </div>
      </form>
    </section>
    <!-- Contact End -->
  </div>
</template>

<script>
import emailjs from "emailjs-com";

export default {
  name: "Contact",
  methods: {
    sendEmail() {
      emailjs.sendForm('service_ltpiqkv', 'template_f67hrz9', this.$refs.form, 'user_9JZ1CCmPE0MfzHCdZUSgE')
        .then((result) => {
            console.log('SUCCESS!', result.text);
        }, (error) => {
            console.log('FAILED...', error.text);
        });
    },
  },
};
</script>
