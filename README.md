# yt-dlp - Guia Completo

Guia completo em português para instalação e uso do yt-dlp para download de vídeos do YouTube.

📋 **Índice**
- [Pré-requisitos](#pré-requisitos)
- [Instalação](#instalação)
- [Como Usar](#como-usar)
- [Comandos Avançados](#comandos-avançados)
- [Exemplos Práticos](#exemplos-práticos)
- [Solução de Problemas](#solução-de-problemas)
- [Avisos Importantes](#avisos-importantes)
- [Comandos de Manutenção](#comandos-de-manutenção)
- [Opções de Output](#opções-de-output)
- [Autor](#autor)
- [Licença](#licença)

---

⚙️ **Pré-requisitos**

1.  **Instalar Python**
    - Acesse: [python.org/downloads](https://www.python.org/downloads)
    - Baixe a versão mais recente.
    - Marque a opção: `[x] Add python.exe to PATH`
    - Complete a instalação.

2.  **Verificar Instalação**
    ```bash
    python --version
    pip --version
    ```

---

📥 **Instalação**

- **Instalar yt-dlp via pip**
    ```bash
    pip install yt-dlp
    ```

- **Atualizar para versão mais recente**
    ```bash
    pip install --upgrade yt-dlp
    ```

---

🚀 **Como Usar**

- **Comando Básico**
    ```bash
    yt-dlp [https://www.youtube.com/watch?v=ID_DO_VIDEO](https://www.youtube.com/watch?v=ID_DO_VIDEO)
    ```

- **Baixar em Pasta Específica**
    ```bash
    cd /d D:\pasta_desejada
    yt-dlp URL_DO_VIDEO
    ```

- **Baixar Apenas Áudio (MP3)**
    ```bash
    yt-dlp -x --audio-format mp3 URL_DO_VIDEO
    ```

---

⚡ **Comandos Avançados**

- **Listar Formatos Disponíveis**
    ```bash
    yt-dlp -F URL_DO_VIDEO
    ```

- **Download com Qualidade Específica**
    ```bash
    yt-dlp -f "bestvideo[ext=mp4]+bestaudio[ext=m4a]/best[ext=mp4]/best" --merge-output-format mp4 URL_DO_VIDEO
    ```

- **Download com Nome Personalizado**
    ```bash
    yt-dlp -o "%(title)s - %(uploader)s.%(ext)s" URL_DO_VIDEO
    ```

- **Download de Playlist**
    ```bash
    yt-dlp "URL_DA_PLAYLIST"
    ```

- **Limitar Velocidade de Download**
    ```bash
    yt-dlp --limit-rate 2M URL_DO_VIDEO
    ```

---

💡 **Exemplos Práticos**

- **Exemplo 1: Download para SSD**
    ```bash
    cd /d D:\ssd
    yt-dlp [https://www.youtube.com/watch?v=L9uPaKtLQX4](https://www.youtube.com/watch?v=L9uPaKtLQX4)
    ```

- **Exemplo 2: Download como MP3 de Alta Qualidade**
    ```bash
    yt-dlp -x --audio-format mp3 --audio-quality 0 [https://www.youtube.com/watch?v=L9uPaKtLQX4](https://www.youtube.com/watch?v=L9uPaKtLQX4)
    ```

- **Exemplo 3: Download com Qualidade 1080p**
    ```bash
    yt-dlp -f "bestvideo[height=1080]+bestaudio" --merge-output-format mp4 URL_DO_VIDEO
    ```

---

🔧 **Solução de Problemas**

- **Problema: Comando não reconhecido**
    **Solução:**
    - Verifique se Python foi instalado com "Add to PATH".
    - Reinicie o Prompt de Comando.
    - Teste com: `python -m yt_dlp URL_DO_VIDEO`

- **Problema: Erro de codec/formato**
    **Solução:**
    ```bash
    yt-dlp -f "bestvideo[ext=mp4]+bestaudio[ext=m4a]" --merge-output-format mp4 URL_DO_VIDEO
    ```

- **Problema: Download lento**
    **Solução:**
    - Use limite de velocidade: `--limit-rate 2M`
    - Verifique sua conexão de internet.

---

⚠️ **Avisos Importantes**
- ✅ Use apenas para conteúdo próprio ou com permissão.
- ⚠️ Respeite os direitos autorais dos criadores.
- 🔒 O download pode violar os Termos de Serviço do YouTube.
- 💾 Mantenha backups dos seus arquivos importantes.

---

🔄 **Comandos de Manutenção**

- **Verificar versão instalada**
    ```bash
    yt-dlp --version
    ```

- **Atualizar yt-dlp**
    ```bash
    pip install --upgrade yt-dlp
    ```

- **Verificar sites suportados**
    ```bash
    yt-dlp --list-extractors
    ```

---

📊 **Opções de Output**

- **Estrutura de nomes de arquivo**
    - `%(title)s` - Título do vídeo
    - `%(uploader)s` - Nome do canal
    - `%(upload_date)s` - Data de upload
    - `%(id)s` - ID do vídeo
    - `%(ext)s` - Extensão do arquivo

- **Exemplo:**
    ```bash
    yt-dlp -o "%(uploader)s/%(upload_date)s - %(title)s.%(ext)s" URL_DO_VIDEO
    ```

---

👨‍💻 **Autor**
- Seu Nome
- GitHub: `@seuusuario`

---

📄 **Licença**
Este guia é disponibilizado apenas para fins educacionais. O uso do yt-dlp está sujeito aos termos de serviço das plataformas.
Use com responsabilidade!
