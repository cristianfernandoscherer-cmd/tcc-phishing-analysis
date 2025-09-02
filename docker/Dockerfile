FROM n8nio/n8n:latest

# Corrige o caminho do comando
ENTRYPOINT ["/usr/local/bin/n8n"]

# Configurações de ambiente
ENV N8N_PORT=5678
ENV N8N_PROTOCOL=http
ENV N8N_ENFORCE_SETTINGS_FILE_PERMISSIONS=true

# Cria diretórios necessários
RUN mkdir -p /home/node/.n8n && \
    chown -R node:node /home/node/.n8n

# Usuário correto
USER node

# Expõe a porta
EXPOSE 5678
