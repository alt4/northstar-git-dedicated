FROM ghcr.io/pg9182/northstar-dedicated:1-tf2.0.11.0

USER root
# Go to location
RUN cd /usr/lib/northstar/R2Northstar/
# Get zip
RUN wget https://github.com/alt4/NorthstarMods/archive/refs/heads/ctf-fixes.zip
# Remove old mods, unzip new, rename folder, then cleanup
RUN rm -rf mods/ \
    && unzip main.zip \
    && mv NorthstarMods-main/ mods \
    && rm main.zip \
    && cd mods \
    && rm -rf LICENSE Northstar.Coop/ README.md .gitattributes .gitignore

USER northstar
EXPOSE 8081/tcp
EXPOSE 37015/udp

ENTRYPOINT ["/usr/libexec/nsdedi", "                                                                                                                        "]
