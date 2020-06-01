<template>
  <Layout>
     <Author :show-title="true" />
<div class=" content has-text-centered">
<p>Projektet RedMic är inriktat mot att utveckla tekniker och strategier för att minska utsläppen av miljöföroreningar från enskilda avlopp.
De övergripande målen är att</p>


1. identifiera och kvantifiera utsläppen av miljöföroreningar från enskilda avlopp.<br>
2. utveckla och utvärdera nya innovativa reningstekniker. <br>
3. identifiera viktiga källor av miljöföroreningar i privata hushåll. <br>
4. ta fram en effektiv strategi för minskning av diffusa utsläpp från privata hushåll. <br>

</div>
  </Layout>
</template>

<script>
import Author from '~/components/Author.vue';
export default {
   components: {
    Author
  },
  metaInfo: {
    title: 'Om RedMic',
  },
};
</script>
