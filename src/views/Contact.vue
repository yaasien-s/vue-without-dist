<template>
    <section id="contact">
        <div class="contact">
            <h1 class="display-4 contact-heading">Contact</h1>

            <div class="container">
                <div class="row">
                    <div class="contact-text col-sm-6">
                        <div class="text-box-inline">
                            <h2>
                                Have You Any Project?
                                <br>
                                Please Drop a Message
                            </h2>
                            <p>
                                Get in touch and let me know how i can help. Fill out the form and i’ll be in touch as
                                soon as
                                possible.
                            </p>
                        </div>
                        <ul class="contact-info">
                            <li>
                                <div>
                                    <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor"
                                        class="bi bi-geo-alt-fill mx-3" viewBox="0 0 16 16">
                                        <path
                                            d="M8 16s6-5.686 6-10A6 6 0 0 0 2 6c0 4.314 6 10 6 10zm0-7a3 3 0 1 1 0-6 3 3 0 0 1 0 6z" />
                                    </svg>
                                    <strong>Address:</strong>
                                    <p id="contact-address">Cape Town, Western Cape, South Africa</p>
                                </div>
                            </li>
                            <li>
                                <div>
                                    <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor"
                                        class="bi bi-telephone mx-3" viewBox="0 0 16 16">
                                        <path
                                            d="M3.654 1.328a.678.678 0 0 0-1.015-.063L1.605 2.3c-.483.484-.661 1.169-.45 1.77a17.568 17.568 0 0 0 4.168 6.608 17.569 17.569 0 0 0 6.608 4.168c.601.211 1.286.033 1.77-.45l1.034-1.034a.678.678 0 0 0-.063-1.015l-2.307-1.794a.678.678 0 0 0-.58-.122l-2.19.547a1.745 1.745 0 0 1-1.657-.459L5.482 8.062a1.745 1.745 0 0 1-.46-1.657l.548-2.19a.678.678 0 0 0-.122-.58L3.654 1.328zM1.884.511a1.745 1.745 0 0 1 2.612.163L6.29 2.98c.329.423.445.974.315 1.494l-.547 2.19a.678.678 0 0 0 .178.643l2.457 2.457a.678.678 0 0 0 .644.178l2.189-.547a1.745 1.745 0 0 1 1.494.315l2.306 1.794c.829.645.905 1.87.163 2.611l-1.034 1.034c-.74.74-1.846 1.065-2.877.702a18.634 18.634 0 0 1-7.01-4.42 18.634 18.634 0 0 1-4.42-7.009c-.362-1.03-.037-2.137.703-2.877L1.885.511z" />
                                    </svg>
                                    <strong>Phone:</strong>
                                    <ul>
                                        <li><a href="tel:0615053706" class="ltr-dir">061 505 3706</a></li>
                                    </ul>
                                </div>
                            </li>
                            <br>
                            <li>
                                <div>
                                    <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor"
                                        class="bi bi-envelope mx-3" viewBox="0 0 16 16">
                                        <path
                                            d="M0 4a2 2 0 0 1 2-2h12a2 2 0 0 1 2 2v8a2 2 0 0 1-2 2H2a2 2 0 0 1-2-2V4Zm2-1a1 1 0 0 0-1 1v.217l7 4.2 7-4.2V4a1 1 0 0 0-1-1H2Zm13 2.383-4.708 2.825L15 11.105V5.383Zm-.034 6.876-5.64-3.471L8 9.583l-1.326-.795-5.64 3.47A1 1 0 0 0 2 13h12a1 1 0 0 0 .966-.741ZM1 11.105l4.708-2.897L1 5.383v5.722Z" />
                                    </svg>
                                    <strong>Email:</strong>
                                    <ul>
                                        <li><a href="mailto:info@nafie.com">yaasiensalaam.com</a></li>
                                    </ul>
                                </div>
                            </li>
                        </ul>

                    </div>
                    <div class="form col-sm-5">
          <form
            id="contact-form"
            action="https://formspree.io/f/xpzbprkz"
            method="POST"
            target="_blank"
          >
            <label>Name</label>
            <input type="text" class="w-100 mx-0" placeholder="John Doe" required />
            <label>E-mail</label>
            <input type="email" class="w-100 mx-0" placeholder="johndoe@gmail.com" name="_replyto" required />
            <label>Message</label>
            <textarea name="textarea" placeholder="Hi there..." required class="w-100 h-25"></textarea>
            <button type="submit" class="btn" id="Send">Send</button>
          </form>
        </div>
                </div>
            </div>
            <router-link to="/" id="home"><svg xmlns="http://www.w3.org/2000/svg" width="40" height="40" fill="#fff"
                    class="bi bi-house-fill" viewBox="0 0 16 16">
                    <path fill-rule="evenodd"
                        d="m8 3.293 6 6V13.5a1.5 1.5 0 0 1-1.5 1.5h-9A1.5 1.5 0 0 1 2 13.5V9.293l6-6zm5-.793V6l-2-2V2.5a.5.5 0 0 1 .5-.5h1a.5.5 0 0 1 .5.5z" />
                    <path fill-rule="evenodd"
                        d="M7.293 1.5a1 1 0 0 1 1.414 0l6.647 6.646a.5.5 0 0 1-.708.708L8 2.207 1.354 8.854a.5.5 0 1 1-.708-.708L7.293 1.5z" />
                </svg></router-link>
        </div>
    </section>
</template>

<script>
    export default {
       
    }
</script>

<style>
    #contact {
        margin-top: 100px;
    }

    .contact {
        width: 90%;
        display: flex;
        flex-direction: column;
        color: #000;
        border-radius: 5px;
        box-shadow: 0 0 10px rgba(0, 0, 0, 25);
        margin-left: auto;
        margin-right: auto;
        margin-bottom: 100px;
        padding-bottom: 100px;
    }

    .contact-heading {
        margin-top: 75px;
    }

    form {
        max-width: 420px;
        margin: 30px auto;
        background: #2b2b26;
        text-align: left;
        padding: 40px;
        border-radius: 10px;
        margin-top: 70px;
        height: 500px;
        border: 1px solid #2b2b26;
        margin-top: 100px !important;
        box-shadow: 0 0 10px rgba(0, 0, 0, 25);
    }

    .contact-text {
        margin-top: 175px !important;
        text-align: initial;
    }

    label {
        color: #568259;
        display: inline-block;
        margin: 17px 0 15px;
        font-size: 0.8em;
        text-transform: uppercase;
        letter-spacing: 1px;
        font-weight: bold;
        margin-left: 20px;
        font-weight: 600;
    }

    input {
        display: block;
        padding: 10px 6px;
        width: 100%;
        box-sizing: border-box;
        border: #568259 1px solid;
        border-bottom: 1px solid #568259 !important;
        color: #568259;
        border-radius: 10px;
        background: #568259;
        box-shadow: 0 0 10px rgba(0, 0, 0, 25);
    }

    ::placeholder {
        color: #fff;
        font-weight: 300;
        padding-left: 10px;
        opacity: 0.5;
    }

    input,
    select {
        display: block;
        padding: 10px 6px;
        width: 85%;
        margin-right: auto;
        margin-left: 30px !important;
        box-sizing: border-box;
        border-bottom: 1px solid #ddd;
        color: #2b2b26;
        border-radius: 10px;
        font-weight: 600;
    }

    input[type="checkbox"] {
        display: inline-block;
        width: 16px;
        margin: 0 10px 0 0;
        position: relative;
        top: 2px;
    }

    .pill {
        display: inline-block;
        margin: 20px 10px 0 0;
        padding: 6px 12px;
        background: #eee;
        border-radius: 20px;
        font-size: 12px;
        font-weight: bold;
        color: #2b2b26;
        cursor: pointer;
    }

    #Send {
        background: #568259;
        border: 0;
        padding: 10px 20px;
        margin-top: 20px;
        color: #2b2b26;
        border-radius: 5px !important;
        cursor: pointer;
        font-weight: 600;
        box-shadow: rgba(48, 48, 48, 0.25) 0px 30px 60px -12px inset, rgba(0, 0, 0, 0.3) 0px 18px 36px -18px inset;
    }
    textarea {
        background: #568259;
        border-radius: 10px;
        box-shadow: 0 0 10px rgba(0, 0, 0, 25);
    }

    #Send:hover {
        background: #2b2b26;
        color: #568259;
        /* border: #568259 1px solid; */
        box-shadow: rgba(0, 0, 0, 0.17) 0px -23px 25px 0px inset, rgba(0, 0, 0, 0.15) 0px -36px 30px 0px inset, rgba(0, 0, 0, 0.1) 0px -79px 40px 0px inset, rgba(0, 0, 0, 0.06) 0px 2px 1px, rgba(0, 0, 0, 0.09) 0px 4px 2px, rgba(0, 0, 0, 0.09) 0px 8px 4px, rgba(0, 0, 0, 0.09) 0px 16px 8px, rgba(0, 0, 0, 0.09) 0px 32px 16px;
    }

    button:hover {
        opacity: 0.8;
    }

    .text-box-inline {
        color: #2b2b26;
    }

    .text-box-inline p {
        font-weight: 600;
    }

    .text-box-inline h2 {
        font-weight: 600;
    }

    strong {
        color: #2b2b26;
    }

    li a {
        color: #2b2b26;
        text-decoration: none;
        font-weight: 600;
    }

    li a:hover {
        color: #2b2b26;
        text-decoration: underline;
    }
    li {
        list-style-type: none;
    }

    #contact-address {
        font-weight: 600;
    }
</style>