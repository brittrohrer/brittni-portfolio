<script setup>
useHead({
    title: 'Brittni Rohrer | Contact Page',
    meta: [
        {name: 'description', content: 'Email contact form to send a message'}
    ]
})
const contactTitle = ref("Contact Me");

</script>
<template>
    <main class="page">
        <h2 class="page__title">{{ contactTitle }}</h2>
    
        <section>
            <div class="contact-form__container">
                <h3 class="contact-form__title">Send A Message</h3>
                <form class="contact-form">
                    <div class="contact-form__item">
                        <label for="name"
                               class="form__label">
                               Full Name:</label>
                        <input type="text"
                               name="name"
                               id="name"
                               required
                               class="form__input"
                               placeholder="Your Name">
                    </div>

                    <div class="contact-form__item">
                        <label for="email"
                               class="form__label">
                               Email:</label>
                        <input type="email"
                               name="email"
                               id="email"
                               required
                               class="form__input"
                               placeholder="Your Email">
                    </div>

                    <div class="contact-form__item">
                        <label for="subject"
                               class="form__label">
                               Subject:</label>
                        <input type="text"
                               name="subject"
                               id="subject"
                               required
                               class="form__input"
                               placeholder="Email Subject">
                    </div>

                    <div class="contact-form__item">
                        <label for="message"
                               class="form__label">
                               Message:</label>
                        <textarea name="message"
                                  id="message"
                                  required
                                  class="form__input form__input--message"
                                  placeholder="Your Message"></textarea>
                    </div>

                    <div class="contact-form__item">
                        <button class="form__button" type="submit">Send</button>
                    </div>
                </form>
            </div>
        </section>
    </main>
</template>