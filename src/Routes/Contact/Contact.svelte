<script>
    import emailjs from 'emailjs-com';
  
    let name = '';
    let email = '';
    let message = '';
    emailjs.init(import.meta.env.VITE_EMAILJS_PUBLIC_KEY)

    function sendEmail(event) {
      event.preventDefault();
  
      emailjs.send(
        'service_kbjw5e8',  // Replace with your service ID
        'template_xz4z168', // Replace with your template ID
        {
          from_name: name,
          reply_to: email,
          message: message,
        }
      )
      .then(response => {
        console.log('Email sent successfully!', response.status, response.text);
        // You can add a success message or reset form fields here
      })
      .catch(error => {
        console.error('Failed to send email:', error);
        // Handle errors here
      });
    }
    
  </script>

<section class="padding16px">
    <div class="grid-5columns">
        <!-- {/* Data */} -->
        <div class="grid-rows grid-span-2-column">
            <div class="padding16px">
                <div>
                    <span class="material-symbols-outlined">chat_bubble</span>
                    <p class="fw-bold">Chat with us</p>
                </div>
                <div><p class="fs-500">Our team is here to help</p></div>
                <div><p class="fs-500">heartofwisdomsaugltd@gmail.com</p></div>
            </div>
            <div class="padding16px">
                <div>
                    <span class="material-symbols-outlined">pin_drop</span>
                    <p class="fw-bold">Areas of operation</p>
                </div>
                <div><p class="fs-500">Where do we work from</p></div>
                <div>
                    <p class="fs-500">
                        Kasese district, Mawokota south, butambala, Kampala, Eastern region, disaster affected and poverty stricken communities in Uganda.
                    </p>
                </div>
            </div>

            <div class="padding16px">
                <div>
                    <span class="material-symbols-outlined">pin_drop</span>
                    <p class="fw-bold">Visit us</p>
                </div>
                <div><p class="fs-500">Come say hello to our team</p></div>
                <div>
                    <p class="fs-500">
                        Makerere Kagugube, P.O. Box, 154814 Kampala- Uganda.
                    </p>
                </div>
            </div>
            <div class="padding16px">
                <div>
                    <span class="material-symbols-outlined">phone_in_talk</span>
                    <p class="fw-bold">Call us</p>
                </div>
                <div><p class="fs-500">Mon-Fri 8am to 5pm</p></div>
                <div><p class="fs-500">Phone: +256756547236</p></div>
            </div>
        </div>
        <!-- {/* Form */} -->
        <div
            class="grid-rows2 grid-span-3-column reverse-on-mobile BLUE rounded-1rem padding16px"
        >
            <form on:submit={sendEmail}>
                <div>
                    <p class="fs-secondary-heading text-primary-400 fw-bold">
                        We're here to answer your questions and provide more
                        information about our work.
                    </p>
                </div>
                <div>
                    <p class="text-primary-400 fs-500">
                        Tell us more about your self and what you've got in mind,
                    </p>
                </div>
                <div class="form__group field">
                    <input
                        class="form__field"
                        type="text"
                        name="Name"
                        placeholder={"Name"}
                        id="Name"
                        minlength="2"
                        required
                        bind:value={name}
                    />
                    <label for="name" class="form__label">Name</label>
                </div>
                <div class="form__group field">
                    <input
                        class="form__field"
                        type="email"
                        name="email"
                        id="email"
                        placeholder="You@email.com"
                        required
                        bind:value={email}
                    />
                    <label for="email" class="form__label">Email</label>
                </div>
                ‌
                <div class="form__group field">
                    <textarea
                        class="form__field"
                        name="Message"
                        id="message"
                        cols={30}
                        rows={8}
                        placeholder="Your message"
                        required
                        bind:value={message}
                    ></textarea>
                    <label for="message" class="form__label">Message</label>
                </div>
                <div>
                    <button class="button-dark" type="submit">Submit</button>
                </div>
            </form>
        </div>
    </div>
</section>

<style>
    input{
        outline: 3px solid hsl(203,30%,26%);
        width: 100%;
        height: 5rem;
        line-height: 5rem;
        border-radius: 0.625rem;
        background: transparent;
        transition: 0.1s ease;
        padding: 0.4rem;
    }
    textarea{
        outline: 3px solid hsl(203,30%,26%);
        border-radius: 0.625rem;
        background: transparent;
        width: 100%;
        transition: 0.1s ease;
        padding: 0.4rem;
    }
    input:not(:placeholder-shown):valid{
        outline-color: aqua;
        border: aqua;
    }
    input:not(:placeholder-shown):invalid{
        outline-color: crimson;
        border: crimson;
        
    }
    input:focus:invalid{
        outline-color: burlywood;
        border: burlywood;
        
    }
    @media (min-width: 51em) {
        .grid-5columns {
            display: grid;
            grid-template-columns: 1fr 1fr 1fr 1fr 1fr;
        }
        .grid-span-2-column {
            grid-column: span 2;
        }
        .grid-span-3-column {
            grid-column: span 3;
        }
    }
</style>
