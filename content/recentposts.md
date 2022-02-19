+++
title = "Recent Posts"
date = "2014-04-09"
menu = "main"
+++


<html lang="en">
    <head>
        <meta charset="utf-8">
        <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">
    </head>
    <body>
        <nav class="navbar fixed-top navbar-expand-md navbar-dark bg-dark py-1 top-nav">
            <div class="container">
                    {{ partial "navbar-brand" . }}
                <button class="navbar-toggler collapsed" type="button" data-toggle="collapse" data-target="#navbarCollapse" aria-controls="navbarCollapse" aria-expanded="false" aria-label="Toggle navigation">
                    <i class="fas fa-bars"></i>
                </button>
                <div class="navbar-collapse collapse" id="navbarCollapse">
                    <ul class="navbar-nav mr-auto">
                        {{ partial "top-nav-text-links" . }}
                    </ul>
                    <div class="social-icons d-none d-lg-block">
                        {{ partial "social-icons" . }}
                    </div>
                </div>
            </div>
        </nav>
        {{ range first 8 (where (where .Site.RegularPages "Type" "in" site.Params.mainSections) ".Params.hidden" "!=" true) }}
        <a href="{{ .Permalink }}" class="nav-link">{{ .Title }}</a>
        {{ end }}
    </body>
</html>

Cabbages in the morning
