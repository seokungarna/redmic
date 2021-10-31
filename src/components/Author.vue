<template>
  <div class="author content has-text-centered">
    <g-image
      alt="Om RedMic"
      class="image"
      src="~/assets/images/grasmatta.jpg"
    />

    <h1 v-if="showTitle">
      {{ $static.metadata.siteName }}
    </h1>

    <p>RedMic-projektet finansieras av FORMAS och syftar till att identifiera kritiska organiska mikroföroreningar som släpps ut från reningsanläggningar på plats (OSSF) och tillhandahåller nya vetenskapligt baserade reduktionsverktyg och reduktionsstrategier. <br>
    Närmare 700 000 privata hushåll i Sverige är inte anslutna till någon central reningsanläggning och utsläppen av organiska mikroföroreningar från OSSF är i stort sett okända..</p>
  </div>
</template>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<script>
export default {
  props: {
    showTitle: {
      type: Boolean,
      default: true,
    },
  },
};
</script>
