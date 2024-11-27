<template>
  <footer>
    <div class="footer-left">
      <div class="contact">
        <h3>CONTACT US</h3>
        <p>+44 0161 123 4567</p>
        <p>Email Us</p>
        <p>Mon-Fri 9am-5pm</p>
      </div>

      <div class="customers">
        <h3>CUSTOMERS</h3>
        <p>Start a Return</p>
        <p>Return Policy</p>
        <p>FAQ</p>
        <p>Catalogs and Mailers</p>
        <p>About Group Gifting</p>
      </div>

      <div class="company">
        <h3>COMPANY</h3>
        <p>About Us</p>
        <p>Sustainability</p>
        <p>Discover Revive</p>
        <p>Careers</p>
        <p>Privacy Policy</p>
        <p>Terms</p>
      </div>

    </div>


    <div class="footer-right">
      <h4>Get the latest new from us</h4>

      <input type="text" placeholder="Enter your email address">
      <p>By signing up, you agree to our <a href="">Privacy Policy</a> and <a href="">Terms of Service</a>.</p>

      <button>Subscribe</button>
    </div>

  </footer>

</template>


<script setup>

</script>


<style scoped>

  footer {
    display: flex;
    justify-content: space-between;
    background: rgb(240, 238, 223);
    padding: 100px 40px 50px 40px;
  }

  .footer-left {
    display: flex;
    flex-direction: row;
    width: 100%;
    gap: 60px;
  }

  .footer-left h3 {
    padding-bottom: 30px;
    font-family: "Hubot Sans", sans-serif;
    font-size: 14px;
    font-weight: 600;
    letter-spacing: .8px;
    color: #909090;
  }

  .footer-left p, .footer-right p {
    font-family: 'montserrat', sans-serif;
    font-size: 14px;
    font-weight: 600;
    color: #515151;
    letter-spacing: .8px;
    padding: 3px 0;
  }

  .footer-right {
    display: flex;
    flex-direction: column;
    padding-right: 20px;
  }

  .footer-right h4 {
    font-family: 'montserrat', sans-serif;
    font-size: 16px;
    font-weight: 600;
    color: #515151;
    padding-bottom: 30px;
  }

  .footer-right input {
    padding: 10px 15px;
    border: 0.5px solid #515151;
    color: #515151;
    width: 420px;
    font-size: 14px;
  }

  .footer-right input:focus {
    outline: none;
  }

  .footer-right a {
    color: #515151;
  }

  .footer-right button {
    padding: 10px 20px;
    border: none;
    background: #515151;
    color: #fff;
    font-family: 'montserrat', sans-serif;
    font-size: 14px;
    font-weight: 600;
    margin-top: 30px;
    cursor: pointer;
    box-sizing: border-box;
    width: auto;
    max-width: 200px;
    align-self: start;
  }

  @media screen and (max-width: 1200px) {
    .footer-left {
      gap: 30px;
    }

    .footer-right {
      /* display: flex;
      flex-direction: column; */
      padding-right: 0px;
    }

    .footer-right input {
      width: 350px;
    }
  }

  @media screen and (max-width: 1000px) {

    footer {
      /* display: flex;
      justify-content: space-between;
      background: rgb(240, 238, 223); */
      padding: 100px 30px 50px 30px;
    }

    .footer-left {
      gap: 20px;
    }

    .footer-left h3 .footer-right h4 {
      /* padding-bottom: 30px;
      font-family: "Hubot Sans", sans-serif; */
      font-size: 12px;
      /* font-weight: 600;
      letter-spacing: .8px;
      color: #909090; */
    }

    .footer-left p, .footer-right p {
      /* font-family: 'montserrat', sans-serif; */
      font-size: 12px;
      /* font-weight: 600;
      color: #515151;
      letter-spacing: .8px;
      padding: 3px 0; */
    }

    .footer-right input {
      max-width: 300px;
      width: 100%;
    }
  }

  @media screen and (max-width: 800px) {

    footer {
      flex-direction: column;
      gap: 40px;
    }

    .footer-left {
      /* display: flex;
      flex-direction: row; */
      justify-content: space-around;
      /* width: 100%; */
      /* gap: 60px; */
    }

    .footer-right {
      /* display: flex; */
      flex-direction: column;
      align-items: center;
      text-align: center;
      /* padding-right: 20px; */
    }

    .footer-right h4 {
      /* font-family: 'montserrat', sans-serif;
      font-size: 16px;
      font-weight: 600;
      color: #515151; */
      padding-bottom: 10px;
    }

    .footer-right button {
      /* padding: 10px 20px;
      border: none;
      background: #515151;
      color: #fff;
      font-family: 'montserrat', sans-serif;
      font-size: 14px;
      font-weight: 600;
      cursor: pointer;
      box-sizing: border-box;
      width: auto;
      max-width: 200px; */
      margin-top: 15px;
      align-self: center;
    }
  }

  @media screen and (max-width: 500px) {

    footer {
      /* display: flex;
      justify-content: space-between;
      background: rgb(240, 238, 223); */
      padding: 70px 30px 50px 30px;
    }

    .footer-left {
      /* display: flex;
      flex-direction: row; */
      justify-content: space-around;
      /* width: 100%; */
      /* gap: 60px; */
      flex-direction: column;
      gap: 50px;
    }

    .footer-left h3 {
      padding-bottom: 15px;
      /* font-family: "Hubot Sans", sans-serif; */
      font-size: 16px;
      /* font-weight: 600;
      letter-spacing: .8px;
      color: #909090; */
    }

    .footer-left p {
      font-size: 14px;
    }

    .footer-right input {
      max-width: 350px;
      /* width: 100%; */
    }
  }
</style>
