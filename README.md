# Upload SFTP Automático

Este projeto em Python realiza o envio automático de arquivos de uma pasta local para um servidor SFTP. Ideal para rotinas de integração entre sistemas ou backup remoto.

## 🔧 Funcionalidades

- Verifica se há arquivos disponíveis em uma pasta local
- Envia o primeiro arquivo encontrado para um diretório remoto via SFTP
- Ignora verificação de host key (útil para ambientes de teste)

## 📦 Requisitos

- Python 3.7+
- Bibliotecas:
  - `pysftp`
  - `os`
  - `warnings`
  - `shutil`

Instale o `pysftp` com:

```bash
pip install pysftp
