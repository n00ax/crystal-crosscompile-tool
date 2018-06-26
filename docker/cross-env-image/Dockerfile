ARG target_architecture_name
ARG target_build_commands

FROM multiarch/alpine:${target_architecture_name}-edge

RUN apk add alpine-sdk
RUN apk add crystal
RUN apk add shards
RUN sh -c ":;$target_build_commands"