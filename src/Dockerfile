FROM ghcr.io/pg9182/northstar-dedicated:1-tf2.0.11.0

ARG owner=alt4
ARG ref=ctf-fixes

USER root
# Go to location
RUN cd /usr/lib/northstar/R2Northstar/
# Get zip
RUN wget https://github.com/$owner/NorthstarMods/archive/refs/heads/$ref.zip
# Remove old mods, unzip new, rename folder, then cleanup
RUN rm -rf mods/ \
    && unzip $ref.zip \
    && mv NorthstarMods-$ref/ mods \
    && rm $ref.zip \
    && cd mods \
    && rm -rf LICENSE Northstar.Coop/ README.md .gitattributes .gitignore

USER northstar
EXPOSE 8081/tcp
EXPOSE 37015/udp

ENTRYPOINT ["/usr/libexec/nsdedi", "                                                                                                                        "]
