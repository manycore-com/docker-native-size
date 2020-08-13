#
# docker build -t ehsmeng/smalltest_jvm:latest .
# docker save ehsmeng/smalltest_jvm > smalltest_jvm.tar
#
# docker cleanup: 
# docker image prune --all
#
# gcp specifics:
# https://cloud.google.com/container-registry/docs/quickstart
#
# --scale-tier BASIC
# Single worker instance. This tier is suitable for learning how to use AI Platform, and for experimenting with new models using small datasets. 
# 
# --master-machine-type
# https://cloud.google.com/ai-platform/training/docs/machine-types
# 
# gcloud ai-platform jobs submit training jobname --scale-tier BASIC --master-machine-type n1-highmem-2 --region us-central1 --master-image-uri gcr.io/refrem-90210/ai-server
#
# docker run ehsmeng/smalltest_jvm:latest 
FROM openjdk:14.0.1-slim

WORKDIR /app

WORKDIR /app

COPY ./smalltest-0.0.1-SNAPSHOT.jar /app

CMD ["java", "-cp", "smalltest-0.0.1-SNAPSHOT.jar", "io.manycore.Main"]
