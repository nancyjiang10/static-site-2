<!--
@component
This is your page!
-->
<script>
  // Import all the news furniture components
  import ArticleHeader from '$lib/components/ArticleHeader.svelte';
  import ArticleBody from '$lib/components/ArticleBody.svelte';
  import Image from '$lib/components/Image.svelte';
  import RelatedLinks from '$lib/components/RelatedLinks.svelte';

  // Article metadata
  let headline = 'Bad Bunny turns Super Bowl halftime into Puerto Rican love letter with Lady Gaga surprise';
  let byline = 'Angelica Medina';
  let pubDate = '2026-02-09';

  // Related stories
  const relatedStories = [
    { headline: 'How America\'s top news organizations escape rigid publishing systems to design beautiful data-driven stories on deadline.', href: 'https://palewi.re/docs/coding-the-news/' },
    { headline: 'How to install, configure and use Visual Studio Code, GitHub and Copilot', href: 'https://palewi.re/docs/coding-the-news/scripts/week-1/' },
    { headline: "How to publish a website with Node.JS and GitHub Actions", href:"https://palewi.re/docs/coding-the-news/scripts/week-2/"},
  ];
</script>

<!-- This sets the page title in the browser tab -->
<svelte:head>
  <title>{headline} | NYCity News Service</title>
  <meta name="description" content="At the Craig Newmark Graduate School of Journalism at the City University of New York, change is in our DNA. That comes of being born in 2006, as the digital revolution was transforming our profession in ways none of us could have imagined." />
</svelte:head>

<!-- Your page content goes here -->
<div class="container">
  
  <!-- Article Header: Headline, byline, and publication date -->
  <ArticleHeader
    {headline}
    {byline}
    {pubDate}
  />

  <!-- Lead Image: Animated gif of students at the journalism school -->
  <Image
    src="/example-photo.gif"
    alt="The Craig Newmark Graduate School of Journalism is at 219 West 40th Street in Midtown Manhattan."
    caption="The Craig Newmark Graduate School of Journalism is at 219 West 40th Street in Midtown Manhattan."
    credit="Craig Newmark Graduate School of Journalism"
  />

  <!-- Article Body: The main story text with proper typography -->
  <ArticleBody>
    <p>
      SANTA CLARA, California, Feb 8 (Reuters) - (This Feb 8 story has been corrected to fix the name of the song to 'Die With A Smile,' not 'If Tomorrow Never Comes,' in the third bullet point)
    </p>

    <p>
Bad Bunny transformed Levi's Stadium into a vibrant homage to Puerto Rico during Sunday's Super Bowl halftime show, delivering a high-energy journey through the island's culture complete with a surprise appearance by Lady Gaga and a tribute from reggaeton pioneer Daddy Yankee.
    </p>

    <p>
The halftime spectacular marked a historic moment for Latin music on America's biggest stage, following last year's record-breaking Kendrick Lamar performance that drew more than 130 million viewers, with Bad Bunny using the platform to celebrate his heritage while cementing reggaeton's place in mainstream American culture.    </p>

    <p>
The choice of Bad Bunny, whose full name is Benito Antonio Martinez Ocasio, to feature in the halftime show drew a rebuke from President Donald Trump and other conservatives over the entertainer's outspoken criticism of U.S. immigration policy.
    </p>

    <p>
On Sunday, Trump said on social media that the Super Bowl halftime show fronted by the singer was "absolutely terrible."
    </p>

    <p>
Clad in a white suit, the 31-year-old superstar opened with "Tití Me Preguntó" while walking through carefully crafted vignettes of Puerto Rican life - farmers in traditional pava hats, domino players, and boxers.
    </p>

    <p>
The performance hit its stride at a secondary stage dubbed "La Casita" (the little house), where he sang "Yo Perreo Sola," "Safaera" and "Party" as celebrities including Pedro Pascal, Karol G, Cardi B and Jessica Alba were spotted dancing in the crowd.
    </p>

    <p>
In one of the show's most theatrical moments, Bad Bunny crashed through the ceiling of "La Casita" while performing "Voy a Llevarte Pa' PR," then moved to a white truck where dancers grooved to a medley honoring reggaeton's roots - Daddy Yankee's "Gasolina," Don Omar's "Dale Don Dale" and his own hit "EoO."
    </p>

    <p>
"If I'm here at the Super Bowl 60 it is because I've never stopped believing in myself," he declared as violins swelled into "Monaco."
    </p>
    <p>A staged wedding featuring the iconic La Rana Concho that was shown on the stadium screens set the scene for Lady Gaga's surprise entrance, with the pop superstar singing a salsa version of "Die With A Smile" before dancing with him "BAILE INoLVIDABLE".
</p>
<p>He then transitioned to "NUEVAYol" as a child and his family were shown watching the Grammy Awards ceremony at which he won Album of the Year - the first time the award was given to a Spanish-language album.
</p>
<p>Ricky Martin emerged for "LO QUE LE PASÓ A HAWAii" as Bad Bunny hoisted the Puerto Rican flag and performed "El Apagón," with the stadium erupting in light before he delivered "CAFé CON RON" and yelled, "God bless America!" as he named all the countries on the continent while a parade of flags was held.
</p>
<p> "The only thing more powerful than hate is love," was shown in the stadium, as he told the audience closing with "DtMF," the title track from his Grammy-winning album "Debí Tirar Más Fotos."
</p> 
<p> The Seattle Seahawks beat the New England Patriots 29-13.

</p>
<p> Reporting by Angelica Medina in Santa Clara; Editing by Peter Rutherford and Thomas Derpinghaus</p>

</ArticleBody>

  <!-- Related Stories: Links to other articles -->
  <RelatedLinks
    title="Related Stories"
    links={relatedStories}
  />

</div>

<style>
  /* Styles here only apply to this page */
  .container {
    padding: var(--spacing-lg) var(--spacing-md);
  }
</style>