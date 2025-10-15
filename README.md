📁 Automação de Upload e Download via SFTP com Conversão de Arquivos
Este repositório contém dois scripts em Python que automatizam o envio e recebimento de arquivos via SFTP, com funcionalidades adicionais como verificação de diretórios e conversão de arquivos CSV para XLSX.

🚀 Funcionalidades
1. upload_sftp.py
Verifica se há arquivos em uma pasta local

Envia o primeiro arquivo encontrado para um diretório remoto via SFTP

Ignora verificação de host key (útil para ambientes de teste)

2. download_sftp_converter.py
Remove e recria o diretório local de destino

Conecta-se ao servidor SFTP e busca arquivos que contenham uma string específica (ex: data de ontem)

Baixa o arquivo mais recente que corresponde ao filtro

Converte o arquivo de .csv (separado por ;) para .xlsx

Exclui o arquivo .csv original após a conversão

📦 Requisitos
Python 3.7+

Bibliotecas:

pysftp

pandas

shutil

datetime

os

warnings

Instale as dependências com:

bash
pip install pysftp pandas
🛠️ Como usar
Upload de Arquivo
Configure o caminho da pasta local (local_upload_dir)

Defina as credenciais e o diretório remoto do servidor SFTP

Execute o script:

bash
python upload_sftp.py
Download e Conversão de Arquivo
Configure o diretório local de destino (local_directory)

Defina as credenciais e o diretório remoto do servidor SFTP

O script buscará arquivos com a data de ontem no nome

Execute o script:

bash
python download_sftp_converter.py
⚠️ Avisos Importantes
Os scripts usam credenciais fictícias e desativam a verificação de host key. Para ambientes de produção, recomenda-se configurar corretamente a verificação de segurança.

Certifique-se de que os diretórios locais tenham permissão de leitura e escrita.

O formato de data usado na busca é dd-mm-aaaa. Ajuste conforme necessário.
