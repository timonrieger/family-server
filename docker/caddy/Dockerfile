FROM caddy:2-builder@sha256:4bdeabce8e79d36b23d1cba7d20598cec2c1117ace960d8ca06071f945e8fc9b AS builder

RUN --mount=type=cache,target=/go/pkg/mod \
    --mount=type=cache,target=/root/.cache/go-build \
    xcaddy build \
    --with github.com/caddy-dns/cloudflare

FROM caddy:2@sha256:844f60b64e4724a5aa8245e019dace0d3f199f7433ce6c57676cb30a920dbad9

COPY --from=builder /usr/bin/caddy /usr/bin/caddy
