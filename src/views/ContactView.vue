<template>
  <div class="contact">
    <h1>This is a contact page</h1>
    <ticket-item> </ticket-item>
  </div>
</template>
<script>
// @ is an alias to /src

import TicketItem from "@/components/TicketItem";

export default {
  name: "ContactView", //hier de benaming van je view meegeven.
  components: {
    TicketItem,
  },
};
</script>
