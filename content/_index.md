+++
date = '{{ .Date }}' // This will be the creation date. You can replace it with a specific date, e.g., "2025-06-13"
draft = false
title = 'Welcome to the Wiki' // Set your desired homepage title here
+++

Welcome to our Wiki!


## Site Pages

Below is a list of other pages on this site:

<ul>
  {{ range .Site.RegularPages }}
    {{ if ne .Permalink $.Permalink }}  // This condition prevents the homepage from listing itself
      <li><a href="{{ .RelPermalink }}">{{ .Title }}</a></li>
    {{ end }}
  {{ end }}
</ul>

