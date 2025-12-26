# Gemfile
source "https://rubygems.org"

# Use GitHub Pages' default gems
gem "github-pages", group: :jekyll_plugins

# Additional plugins (ensure they’re supported by GitHub Pages)
group :jekyll_plugins do
  gem "jekyll-seo-tag"
  gem "jekyll-feed"
  gem "jekyll-paginate"
  gem "jekyll-sitemap"
end

# Windows compatibility (keep as-is)
platforms :mingw, :x64_mingw, :mswin, :jruby do
  gem "tzinfo", ">= 1", "< 3"
  gem "tzinfo-data"
  gem "wdm", "~> 0.1"
end

gem "http_parser.rb", "~> 0.6.0", :platforms => [:jruby]

