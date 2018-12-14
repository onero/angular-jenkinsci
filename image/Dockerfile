# Download base image from jenkinsci project (Debian image)
FROM jenkinsci/jenkins:lts

# Ensure super user
USER root

# Ensure we're operating with latest debian updates
RUN apt-get update
# Install Headless testing tool for Angular E2E tests
RUN DEBIAN_FRONTEND=noninteractive apt-get install xvfb -y
# Get signing key in preparation for installing chrome
RUN wget -q -O - https://dl-ssl.google.com/linux/linux_signing_key.pub | apt-key add -
# Add chrome download location
RUN sh -c 'echo "deb http://dl.google.com/linux/chrome/deb/ stable main" >> /etc/apt/sources.list.d/google.list'
# Run update again to get the chrome update
RUN apt-get update
# Install chrome for E2E testing
RUN DEBIAN_FRONTEND=noninteractive apt-get install google-chrome-stable -y
# Install nano <3
RUN apt-get install nano