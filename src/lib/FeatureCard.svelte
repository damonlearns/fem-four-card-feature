<script>
  let { cardTitle = 'CardTitle',
        cardBody = "This is card's body of text",
        borderColor = "--theme-red",
        iconSelector = "teamBuilder"
  } = $props();
  
  let iconPaths = {
    calculator: import.meta.env.BASE_URL + 'icon-calculator.svg',
    karma: import.meta.env.BASE_URL + 'icon-karma.svg',
    supervisor: import.meta.env.BASE_URL + 'icon-supervisor.svg',
    teamBuilder: import.meta.env.BASE_URL + 'icon-team-builder.svg'
  }
</script>

<style>
  :root {
    --text-title: hsl(234, 12%, 34%);
    --text-main: hsl(212, 6%, 44%);
    --theme-red: hsl(0, 78%, 62%);
    --theme-cyan: hsl(180, 62%, 55%);
    --theme-orange: hsl(34, 97%, 64%);
    --theme-blue: hsl(212, 86%, 64%);
  }
  
  

</style>

<!--
Layout dims
Mobile: 300x250
Desktop: 350x250
border-t-teal-400
-->

<div class="shadow-lg
            max-w-[350px] md:min-w-[350px] min-w-[300px]
            max-h-[250px] min-h-[250px]
            w-full h-full bg-white rounded-sm
            border-t-4 text-left p-6"
     style="border-top-color: var({borderColor})"
>
  <h2 class="text-2xl font-bold text-(--text-title)">{cardTitle}</h2>
  <p class="text-(--text-main) text-sm">{cardBody}</p>
  <div class="flex justify-end object-bottom-right pt-8">
    <img src={iconPaths[iconSelector]} alt="Card Icon">
  </div>

</div>