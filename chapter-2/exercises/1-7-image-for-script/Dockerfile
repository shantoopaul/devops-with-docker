# Start from the ubuntu image
FROM ubuntu:24.04

# Use /usr/src/app as our workdir. The following instructions will be executed in this location.
WORKDIR /usr/src/app

# Execute commands with `/bin/sh -c` prefix.
RUN <<EOF
apt-get update
apt-get install -y curl
EOF

# Copy the script.sh file from this directory to /usr/src/app/ creating /usr/src/app/hello.sh
COPY script.sh .

# Give execute permission
RUN chmod +x ./script.sh

# When running Docker run the command will be ./script.sh
CMD ["./script.sh"]