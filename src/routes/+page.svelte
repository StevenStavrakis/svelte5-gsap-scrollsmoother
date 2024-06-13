<script lang="ts">
  import  SvelteMarkdown from "svelte-markdown";
  const source = `# First Page

## Dapibus Caucason

Lorem markdownum tellus; habebat quod, nunc aras mortale petam cultumque.
Bracchia Caeneus gloria!

1. Prospexit classe frenataque haud
2. Hoc umeros agresti viscera
3. Nectare coniuncti
4. Caligine marito

## Coire iter

Pondere tremulis spectat hastam fidesque in fidem [sacerdos
et](http://www.eunt.io/etlynceus) ignarus, Tydiden timeo virgamque ordine Latona
amare. Pectusque medeatur te cava, formatur tellus mutua.

1. Aeeta quas malis deflent
2. Res est quoniam deos ferit haerenti parientem
3. Possedit ossibus
4. Vestros salutant culpae quinque conplexusque illa mandata
5. Omni videri media ante at vidit est
6. Ore ait conlapsa

Per coniuge *victa habitu* aerias, Clymene concretaque Cephalus. Stupet nec
trahitur amoris inmissa iocos, rogat, fabricator.

## Ne ille

Crudelis sinumque custos finemque illo. Tellure Achivi pulvinaribus fratrem ipse
praebebat turpe amantem, ut cum **figitur fecit**: sanguine.

1. Exanimes orsa
2. De esse cum tempore corpore instar
3. Pennatis procul

Arma ratos, vultus tegitur tu imagine cetera. Dixit ponto baculum, a recursus
oraque ante cui, in parat virgam, polo quod *cum spectare* haec? Cassiope quin
inmissa, oris Stabiasque tela voluntas.

Gratior **munere timeto** pudorem soceri, me tota tura premunt. Atra *ausit una*
partu *donare formae* noluit huius laquei. **Tuas** habet illa revincta
praerupit **timetis** surgis brevis sustollit nostro animoque calculus.
`
</script>

<div class="w-full h-[200vh] bg-blue-100">
  <div class="prose py-32 mx-auto">
    <div class="mx-auto">
      <SvelteMarkdown {source} />
    </div>
  </div>
</div>
