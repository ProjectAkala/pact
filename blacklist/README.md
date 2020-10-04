# Blacklist
---

## Editing the list

Data for the blacklist is sourced from [this spreadsheet](https://spo.ink/pactbl). Need to
make a change? Ask Skadiv or Lego for access in [the Discord](https://spo.ink/pact).

---

## Editing the page

We get blocked by [CORS](https://en.wikipedia.org/wiki/Cross-origin_resource_sharing) when
trying to access the Google Sheet data using a `file:///` URL, so if you're wanting to
test or edit this locally, you'll have to access it on `http://localhost/`.

There are several ways to do this, but I would suggest using [Ruby](https://www.ruby-lang.org/)
and the [Jekyll](https://jekyllrb.com/) gem - this is how GitHub themselves run our site!

All you have to do is [download and install Ruby](https://www.ruby-lang.org/en/downloads/),
add it to your PATH, and then open a shell, navigate to the PACT directory, and run
`gem install jekyll`. Once it completes, you should be able to run `jekyll serve` and the
site will be available at [http://localhost:4000/](http://localhost:4000/). It should
automatically update in a few seconds whenever you make a change to one of the files too,
so it's super convenient!

:warning:**Important note**:warning:: Running `jekyll serve` will create a `.jekyll-cache/`
and `_site/` folder. It's usually best to ignore these and pretend that they don't exist -
don't delete them, don't edit them; just let them be! If you like, you can create a file
named `.gitignore` in the PACT directory and add `_site` and `.jekyll-cache` to it - this
ensures that you won't accidentally commit them.
