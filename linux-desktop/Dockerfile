FROM kasmweb/ubuntu-noble-desktop:1.16.0

# Change settings for easier integration with Instruqt
# Port ending with 443 will trigger Instruqt proxy to use https to communicate with this container
ENV NO_VNC_PORT=6443
# No need to use basic auth because Instruqt will handle the authentication
ENV VNCOPTIONS=-disableBasicAuth

# Fix not able to start vncserver because of missing directory
RUN mkdir -p /home/kasm-user/Desktop/Uploads
