FROM gcr.io/cloud-builders/gcloud-slim

RUN apt-get update && apt-get install -y ruby ruby-dev build-essential
RUN gem install jekyll bundler

# this builder assumes user is using jekyll via ruby bundle
# note that bundle's default task is install
ENTRYPOINT ["bundle"]
