# See https://tox.wiki/en/latest/faq.html#running-within-a-docker-container
#
# To run dockerized tests locally, from the root of this project run:
#   docker build --tag 'tox-local' tests
#   docker run -v `pwd`:/tests -it --rm tox-local -e dj42

FROM 31z4/tox

USER root

RUN set -eux; \
    apt-get update; \
    DEBIAN_FRONTEND=noninteractive \
    apt-get install -y --no-install-recommends \
        gettext; \
    rm -rf /var/lib/apt/lists/*

USER tox