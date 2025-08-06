<script>
  import FeatureCard from "./lib/FeatureCard.svelte";
</script>


<main class="bg-[#FAFAFA]">
  <h2 class="font-light md:text-4xl text-2xl md:p-2">Reliable, Efficient Delivery</h2>
  <h2 class="font-bold md:text-4xl text-2xl p-4 md:pt-2 pt-0">Powered by Technology</h2>
  <div class="flex justify-center pb-16">
    <p class="max-w-[500px] text-sm">Our Artificial Intelligence powered tools use millions of project data points
      to ensure that your project is successful</p>
  </div>
  <div class="features-grid">
    <div class="content-center">
      <FeatureCard
          cardTitle="Supervisor"
          cardBody="Monitors activity to identify project roadblocks"
          borderColor="--theme-cyan"
          iconSelector="supervisor"
      />
    </div>
    <div class="flex flex-col gap-8">
      <FeatureCard
          cardTitle="Team Builder"
          cardBody="Scans our talent network to create the optimal team for your project"
      />
      
      <FeatureCard
          cardTitle="Karma"
          cardBody="Regularly evaluates our talent to ensure quality"
          borderColor="--theme-orange"
          iconSelector="karma"
      />
    </div>
    <div class="content-center">
      <FeatureCard
          cardTitle="Calculator"
          cardBody="Uses data from past projects to provide better delivery estimates"
          borderColor="--theme-blue"
          iconSelector="calculator"
      />
    </div>
  
  </div>
</main>

<style>
  .features-grid {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    gap: 2rem;
    max-width: 1200px;
    margin: 0 auto;
    /* Prevent overflow horizontally */
    box-sizing: border-box;
    width: 100%;
    /* Optionally add a min-width to cards for small screens */
  }
  
  .content-center {
    display: flex;
    align-items: center;
    /* This will help with vertical alignment on desktop */
  }
  
  .features-grid > .flex {
    /* nothing needed, already flex-col */
  }
  
  @media (max-width: 640px) {
    .features-grid {
      grid-template-columns: 1fr; /* Single column */
      gap: 2rem;
      padding: 0 1rem;            /* Some horizontal breathing room */
    }
    .content-center,
    .features-grid > .flex {
      justify-content: center;    /* Horizontally center cards */
      align-items: stretch;       /* Stretch cards to full width */
    }
  }
  
  

</style>
