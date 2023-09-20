FROM alpine:latest@sha256:958f4196fcbf9ef8afbef9884c934323f80e4592a12ca4919324881cc832f708 as builder
RUN apk --no-cache add ca-certificates wget unzip
RUN wget -O jacoco.zip http://search.maven.org/remotecontent?filepath=org/jacoco/jacoco/0.8.5/jacoco-0.8.5.zip && unzip jacoco.zip

FROM openjdk:8-jre-slim

COPY --from=builder lib/jacococli.jar /
