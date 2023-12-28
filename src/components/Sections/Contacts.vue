<template>
  <section class="contacts__container" id="contact">
    <div class="contacts__header">
      <div>
        <h2>Contact</h2>
        <span>📧</span>
      </div>
      <span>{{ contactPara }}</span>
    </div>
    <div class="contacts" v-for="(items, index) in contacts" :key="index">
      <div>
        <img
          :src="items.contactImage"
          :alt="items.contactAlt"
          class="contact__icon"
        />
        <div class="contact__email">
          <span>{{ items.spanOne }} </span>
          <span>{{ items.spanTwo }}</span>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import gmailImage from "/src/assets/gmail.png";
import phoneCallImage from "/src/assets/phone-call.png";
export default {
  data() {
    return {
      contactPara: "Want to talk about your next project?",
      contacts: [
        {
          contactImage: gmailImage,
          contactAlt: "Gmail Icon",
          spanOne: "Email:",
          spanTwo: "jamesanquillano@gmail.com",
        },
        {
          contactImage: phoneCallImage,
          contactAlt: "Phone Icon",
          spanOne: "Phone:",
          spanTwo: "09369533064",
        },
      ],
    };
  },
};
</script>
