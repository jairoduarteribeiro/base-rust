FROM rust:1.82.0

RUN groupadd --gid 1000 dev && \
    useradd --uid 1000 --gid dev --shell /bin/bash --create-home dev

RUN set -eux; \
    apt-get update; \
    apt-get install -y --no-install-recommends \
        vim \
        bash-completion; \
    rm -rf /var/lib/apt/lists/*

USER dev

RUN rustup component add rustfmt clippy
