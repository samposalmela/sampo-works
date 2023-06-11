{{ define "main" }}
  <main aria-role="main">
    <header class="homepage-header">
      <h1>Sampo Salmela</h1>
      {{ with .Params.subtitle }}
      <span class="subtitle">{{ . }}</span>
      {{ end }}
    </header>
    <div class="homepage-content">
      <!-- Note that the content for index.html, as a sort of list page, will pull from content/_index.md -->
      welcome to my page
    </div>
    <div>
      {{ range first 10 .Site.RegularPages }}
          {{ .Render "summary" }}
      {{ end }}
    </div>
  </main>
{{ end }}