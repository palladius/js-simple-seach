
run-dev:
	MIN_RATING=3.2 node server.js

docker-build:
#docker build -t 2025-ring .
	docker build -t url-ring .

docker-run: # docker-build
	docker run -it -p 8080:8080 url-ring

build-and-run: docker-build docker-run

install:
	gcloud components install cloud-build-local

#	cloud-build-local --config=cloudbuild.yaml --dryrun=true .
# To run a  build: https://github.com/GoogleCloudPlatform/cloud-build-local
# ./cloud-build-local_{linux,darwin}_{386,amd64}-v<latest_tag> --dryrun=false --config=path/to/cloudbuild.yaml path/to/code
cloud-build-local:
	gcloud config set project puffin-tours
	cloud-build-local --config=cloudbuild.yaml --dryrun=false .

cloud-build-submit:
	gcloud config set project puffin-tours
	gcloud builds submit . \
		--service-account projects/puffin-tours/serviceAccounts/js-ring-cloud-builder@puffin-tours.iam.gserviceaccount.com \
		--gcs-log-dir gs://puffin-tours_cloudbuild/

auth:
	gcloud auth login --update-adc

# deploy:
# 	gcloud run deploy url-ring --image europe-west1-docker.pkg.dev/puffin-tours/geocities-ring/url-ring --region europe-west1 --platform managed --allow-unauthenticated
