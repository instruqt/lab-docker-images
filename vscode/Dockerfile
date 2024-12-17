FROM codercom/code-server:4.95.3-debian

RUN sudo apt update && sudo apt install -y \
  curl wget zip git jq build-essential software-properties-common fonts-jetbrains-mono

ARG EXTENSIONS=""
ENV EXTENSIONS=${EXTENSIONS}

COPY files/install_dependencies.sh /install_dependencies.sh
RUN sudo chmod +x /install_dependencies.sh ; /install_dependencies.sh

COPY files/settings.json /home/coder/.local/share/code-server/Machine/settings.json
COPY files/config.yaml /home/coder/.config/code-server/config.yaml

ENV DEFAULT_FOLDER="/home/coder"

COPY files/entrypoint.sh /entrypoint.sh
RUN sudo chmod +x /entrypoint.sh

RUN sudo chown -R coder:coder /home/coder/.local/share/code-server
RUN mkdir -p /home/coder/.local/share/code-server/coder-logs

ENTRYPOINT ["/entrypoint.sh"]