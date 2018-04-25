FROM debian:stretch-slim

ARG HTTP_PROXY
ARG HTTPS_PROXY
ENV HTTP_PROXY=$HTTP_PROXY
ENV HTTPS_PROXY=$HTTPS_PROXY

# Set UID for new generated files
ARG UID

# create owner of generated files
RUN useradd build -u ${UID} 
RUN adduser build sudo
RUN passwd -d build
RUN echo '%sudo ALL=(ALL) NOPASSWD:ALL' >> /etc/sudoers

# All following commands (VOLUME, CMD) should be executed with this user
USER build

# Sourcecode volume
VOLUME /volume

# Define working directory.
WORKDIR /volume
 
# Define default command.
CMD ["/bin/bash"]
