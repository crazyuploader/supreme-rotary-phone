#
# Created by Jugal Kishore --- 2022
#
# Simple Alpine Docker Image non-root user 'worker' and sudo access
#
# Base Image: alpine:3.20.3
FROM alpine:3.21.3

# Add sudo
RUN apk --no-cache add sudo

# Add user
RUN adduser \
    -D \
    -u 1000 \
    worker

# Add worker user to sudoers file
RUN echo 'worker ALL=(ALL) NOPASSWD:ALL' >> /etc/sudoers

# Switch to worker user
USER worker
