FROM ghcr.io/lucernae/devcontainer-nix:flake

ENV USE_DIRENV="true"
ENV USE_FLAKE="true"
ENV INSTALL_ROOT_PACKAGES=""
ENV PREBUILD_DEFAULT_PACKAGE="default.nix"
ENV PREBUILD_NIX_SHELL="shell.nix"
ENV PREBUILD_FLAKE=""
ENV PREBUILD_FLAKE_RUN=""
ENV PREBUILD_FLAKE_DEVELOP=""
ENV ADDITIONAL_NIX_CHANNEL=""
ENV ADDITIONAL_NIX_FLAKE_REGISTRY=""
ENV PREBUILD_HOME_MANAGER=""
ENV PREBUILD_HOME_MANAGER_FLAKE=""


COPY ./nix.conf /etc/nix/nix.conf
COPY library-scripts /library-scripts

# # Add the configuration setting to /etc/nixos/configuration.nix
# RUN echo 'programs.nix-ld.enable = true;' >> /etc/nixos/configuration.nix

# # Apply the changes using nixos-rebuild switch
# RUN nixos-rebuild switch

RUN bash /library-scripts/build/all.sh