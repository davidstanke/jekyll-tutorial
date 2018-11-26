# jekyll-tutorial
A basic site to try using Jekyll on GCB

The build uses a "jekyll" builder, which is created using this Dockerfile:
```
FROM gcr.io/cloud-builders/gcloud-slim

RUN apt-get update && apt-get install -y ruby ruby-dev build-essential
RUN gem install jekyll bundler

# this builder assumes user is using jekyll via ruby bundle
ENTRYPOINT ["bundle","exec","jekyll","build"]
```
(TODO: make a scheduled build to publish the builder on a schedule)

## Status:
2018-11-26: local build works, via `bundle exec jekyll build`. TODO: GCB build!
