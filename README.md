# pyside6-codespacesPOO
Destinado a resolução do problema da atividade 
# Ambiente PySide6 no GitHub Codespaces (Fluxbox + noVNC)

## Correções aplicadas em relação ao tutorial v0.1
- Remoção dos comandos manuais duplicados (`Xvfb`, `x11vnc`, `fluxbox` e `websockify` no `:99`), pois a feature oficial `desktop-lite:1` do `devcontainer.json` já inicializa automaticamente o servidor gráfico, o Fluxbox e o noVNC na porta `6080` usando `DISPLAY=:1`.
- Remoção do parâmetro inexistente `"desktopElement": "fluxbox"` na configuração da feature `desktop-lite:1`.
- Inclusão de `"forwardPorts": [6080]` e das bibliotecas gráficas (`libxcb-*`, `libxkbcommon-x11-0`, `libgl1`, `libegl1`) necessárias para o plugin `xcb` do Qt6 no Debian Bookworm.

## Passo a passo para executar e validar

1. Abra este repositório no **GitHub Codespaces** e aguarde a conclusão automática do `postCreateCommand` (instalação das dependências do sistema e do `PySide6`).
2. No painel inferior, acesse a aba **Ports** (Portas), localize a porta **6080** (`noVNC Desktop`) e clique em **Open in Browser** (ícone do globo).
3. No navegador, acesse o caminho `/vnc.html` ao final da URL, clique em **Connect** e digite a senha padrão:
   ```text
   vscode
