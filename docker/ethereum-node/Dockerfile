FROM ethereum/client-go:stable

WORKDIR /gethnet
COPY datadir datadir/
COPY config.toml .

ENTRYPOINT [ "geth" ]
CMD [\
"--dev",\
"--datadir", "/gethnet/datadir", \
"--mine", \
"--ipcdisable", \
"--dev.period", "0", \
"--unlock", "0x9ca9d2d5e04012c9ed24c0e513c9bfaa4a2dd77f", \
"--password", "/run/secrets/eth_node_passw", \
"--config", "/gethnet/config.toml" \
]