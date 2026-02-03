<!--
  This is your page!
-->
<script>
  // Import all the news furniture components
  import ArticleHeader from '$lib/components/ArticleHeader.svelte';
  import ArticleBody from '$lib/components/ArticleBody.svelte';
  import ImageWithCaption from '$lib/components/ImageWithCaption.svelte';
  import RelatedLinks from '$lib/components/RelatedLinks.svelte';

  // Article metadata
  let headline = 'Raccoons ovetake J-school. Maybe for the best?';
  let byline = 'A raccoon';
  let pubDate = '2026-02-02';

  // Related stories
  const relatedStories = [
    { headline: 'How America\'s top news organizations escape rigid publishing systems to design beautiful data-driven stories on deadline.', href: 'https://palewi.re/docs/coding-the-news/' },
    { headline: 'How to install, configure and use Visual Studio Code, GitHub and Copilot', href: 'https://palewi.re/docs/coding-the-news/scripts/week-1/' },
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

  <!-- Lead Image: CUNY Journalism School building -->
  <ImageWithCaption
    src="https://i.natgeofe.com/k/6289c775-a06c-426a-badb-8d181a55237b/raccoon-grass_4x3.jpg"
    alt="A raccoon."
    caption="An award-winning investigative journalist. Also, yes, a raccoon."
    credit="U.S. Raccoon Observatory"
  />

  <!-- Article Body: The main story text with proper typography -->
  <ArticleBody>
    <p>
      Raccoons have overtaken the graduate school. And we honestly think they're doing a great job.
    </p>

    <p>
      Who would have thought the next generation of intrepid young journalists would be so... creaturely.
    </p>

    <p>
      Oh, there's no reason to "fear" the raccoons. We welcome our new overlords.
    </p>

    <p>
      I'm sure you have some questions. Sadly, our raccoons are not able to speak.
    </p>

    <p>
      I'm sure they have some spare garbage you could borrow, though.
    </p>

    <p>
      One day, we might all wish to be raccoons.
    </p>

    <p>
      Raccoons.
    </p>

    <p>
      Raccoons?
    </p>

    <p>
      Yes, raccoons.
    </p>
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