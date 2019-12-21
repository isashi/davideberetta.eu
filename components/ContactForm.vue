<template>
  <div class="contact_form_section">
    <div class="container">
      <div class="form">
        <h2>Just say Hi!</h2>
        <form
          id="contactform"
          class="gform"
          method="POST"
          data-email="example@email.net"
          action="https://script.google.com/macros/s/AKfycbxWhoa9RG7sMy1z5lITbY7K7c7mhapjKgDW_EA4pKKjkwrHnqNv/exec"
        >
          <div class="form-elements">
            <div class="inputBox">
              <input type="text" name="name_dberetta" id="name_dberetta" placeholder="Your name">
            </div>
            <div class="inputBox">
              <input type="text" name="email_dberetta" id="email_dberetta" placeholder="Your email">
            </div>
            <div class="inputBox">
              <textarea
                form="contactform"
                rows="5"
                cols="50"
                wrap="physical"
                name="message_dberetta"
                id="message_dberetta"
                placeholder="Your message"
              ></textarea>
            </div>
            <div class="inputBox">
              <input type="submit" value="submit" id="submit">
            </div>
          </div>

          <div style="display:none" class="thankyou_message">
            <!-- You can customize the thankyou message by editing the code below -->
            <h2>
              <em>Thanks</em> for contacting us! We will get back to you soon!
            </h2>
          </div>
        </form>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  components: {},
  props: [],
  computed: {}
};
</script>

<style scoped>
.contact_form_section {
  margin: 0;
  padding: 0;
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
  background: linear-gradient(0deg, #000, #333);
  color: #fff;
}

.container {
  position: relative;
  max-width: 800px;
  min-height: 400px;
  background: rgba(255, 255, 255, 0.05);
  box-shadow: 0 5px 15px rgba(0, 0, 0, 1);
}

.container:before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 50%;
  height: 100%;
  background: rgba(255, 255, 255, 0.08);
  pointer-events: none;
}

.container:after {
  content: "";
  position: absolute;
  top: -5px;
  left: -5px;
  right: -5px;
  bottom: -5px;
  background: linear-gradient(45deg, #ff0047, #6eff00);
  pointer-events: none;
  animation: animate 10s linear infinite;
}

@keyframes animate {
  0% {
    filter: blur(60px) hue-rotate(0deg);
  }
  100% {
    filter: blur(60px) hue-rotate(360deg);
  }
}

.form {
  position: absolute;
  width: 100%;
  height: 100%;
  padding: 40px;
  box-sizing: border-box;
  z-index: 1;
}

.form h2 {
  margin: 0;
  padding: 0;
  color: #fff;
  font-size: 24px;
}

.form .form-elements .inputBox {
  width: 100%;
  margin-top: 20px;
}

.form .form-elements .inputBox input {
  width: 100%;
  background: transparent;
  border: none;
  border-bottom: 2px solid #fff;
  outline: none;
  font-size: 18px;
  color: #fff;
  padding: 5px 0;
}

.form .form-elements .inputBox textarea {
  width: 100%;
  background: transparent;
  border: none;
  border-bottom: 2px solid #fff;
  outline: none;
  font-size: 18px;
  color: #fff;
  padding: 5px 0;
}

::placeholder {
  color: #bbb;
}

.form .form-elements .inputBox input:focus::placeholder {
  color: transparent;
  transition: 0.5s;
}

.form .form-elements .inputBox textarea:focus::placeholder {
  color: transparent;
  transition: 0.5s;
}

.form .form-elements .inputBox input[type="submit"] {
  background: #fff;
  color: #000;
  border: none;
  font-weight: 900;
  max-width: 100px;
  cursor: pointer;
}
</style>