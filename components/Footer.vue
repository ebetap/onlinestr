<template>
  <div class="footer">
    <div class="subscribe-newsletter">
      <div class="container">
        <h2>Subscribe to the newsletter and receive a coupon for 10% off</h2>
        <Button onClick="subscribeHandler" label="Subscribe" type="inverted" />
      </div>
    </div>
    <div class="footer-middle">
      <div class="container">
        <div class="item orders">
          <h2>Orders</h2>
          <ul>
            <li>
              <a href="/">My Account</a>
            </li>
            <li>
              <a href="/">Delivery</a>
            </li>
            <li>
              <a href="/">Return Policy</a>
            </li>
          </ul>
        </div>
        <div class="item help">
          <h2>Help</h2>
          <ul>
            <li>
              <a href="/">Customer Service</a>
            </li>
            <li>
              <a href="/">Size Guide</a>
            </li>
            <li>
              <a href="/">Contact Us</a>
            </li>
          </ul>
        </div>
        <div class="item about-us">
          <h2>About Us</h2>
          <ul>
            <li>
              <a href="/">About Us</a>
            </li>
            <li>
              <a href="/">Store Locator</a>
            </li>
          </ul>
        </div>
        <div class="item socmed">
          <div class="container-socmed">
            <a-icon type="instagram" />
          </div>
          <div class="container-socmed">
            <a-icon type="github" />
          </div>
          <div class="container-socmed">
            <a-icon type="google" />
          </div>
        </div>
      </div>
    </div>
    <div class="footer-bottom">
      <div class="container">
        <a href="/">ID / IDR</a>
      </div>
    </div>
  </div>
</template>

<script>
import Button from '@@/components/Button'
export default {
  name: 'Footer',
  components: {
    Button
  },
  methods: {
    subscribeHandler() {
      return true
    }
  }
}
</script>

<style scoped>
.footer {
  background: #f2f2f2;
}
.subscribe-newsletter {
  padding: 16px 0;
  border-bottom: 1px solid #e0e0e0;
}
.subscribe-newsletter .container {
  display: flex;
  justify-content: space-between;
}
.footer-middle {
  padding: 25px 0;
}
.footer-middle .container {
  display: flex;
  justify-content: space-between;
}
.footer-middle .container .item {
  max-width: 20%;
  flex: 0 0 20%;
}
.footer-middle .container .item:last-child {
  max-width: 40%;
  flex: 0 0 40%;
}
.socmed {
  display: flex;
  justify-content: flex-end;
}
.socmed .container-socmed {
  padding: 6px 10px;
  border-radius: 50%;
  background: #bdbdbd;
  align-self: flex-start;
  margin-left: 15px;
  cursor: pointer;
  transition: all ease 0.2s;
  padding-top: 9px;
}
.socmed .container-socmed:hover {
  background: #828282;
}
.socmed .anticon {
  font-size: 1.2rem;
}
.item ul {
  padding-left: 0px;
  list-style: none;
}
.item li {
  margin-top: 5px;
}
.item a {
  color: #828282;
}
.item a:hover {
  text-decoration: underline;
}
.footer-bottom {
  background: #ffffff;
  padding: 9px 0;
}
.footer-bottom .container {
  display: flex;
  justify-content: space-between;
}
.footer-bottom a {
  color: #e0e0e0;
  font-size: 1rem;
}
.footer-bottom a:hover {
  text-decoration: underline;
}
</style>
