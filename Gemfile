source "https://rubygems.org"

require "json"
require "open-uri"
versions = JSON.parse(open("https://pages.github.com/versions.json").read)
gem "github-pages", versions["github-pages"]
gem "jekyll"

group :jekyll_plugins do
    gem "jekyll-sitemap"
end

gem "autoprefixer-rails"
gem "rouge"
gem "facets"
gem "jekyll-assets"
gem "kramdown"
gem "sass"
gem "typogruby"
gem "uglifier"
gem "jekyll-timeago"
gem "jekyll-srcset"
