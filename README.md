# Gebrauch

Diese Vorlage kann als Basis für Dokumente in Deutsch (Schweiz) dienen.

Als Editor ist [Visual Studio Code](https://code.visualstudio.com/download) vorgesehen.

Die Erweiterung [LaTeX Workshop](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop) wird zur Integration von LaTeX genutzt.

Die Erweiterung [LTeX](https://marketplace.visualstudio.com/items?itemName=valentjn.vscode-ltex) wird als Korrekturhilfe genutzt.

# Installation

Die Vorlage unterstützt mehrere Installationsmöglichkeiten.
Alle nutzen TeX Live.

1. Nativ. TeX Live wird auf Windows installiert.
2. WSL-Remote. TeX Live wird in einer WSL virtuellen Maschine installiert.
3. Docker-Remote. Es wird Docker genutzt, um TeX Live in einen Container zu installieren.
4. Docker-Runner. Es wird ein TeX Live Docker-Image heruntergeladen und für jeden Kompiliervorgang gestartet.

## Nativ

Es existiert ein [Installer](https://tug.org/texlive/windows.html) für TeX Live auf Windows.

## WSL

WSL kann in einer mit Administrator gestarteten Kommandozeile mit dem Befehl `wsl --install` installiert werden.

### WSL-Remote

In der WSL virtuellen Maschine kann TeX Live kann mit dem Befehl `sudo apt install texlive-full -y` installiert werden.

Die Erweiterung [Remote - WSL](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-wsl) wird genutzt, um LaTeX Workshop Zugriff auf die Linux Umgebung zu verschaffen.

## Docker

Es existiert ein [Installer](https://docs.docker.com/desktop/install/windows-install/) für Docker auf Windows. Docker auf Windows setzt [WSL](#wsl) voraus.

### Docker-Remote

Die Erweiterung [Remote - Containers](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers) wird genutzt, um LaTeX Workshop Zugriff auf die Container Umgebung zu verschaffen.

Die Konfiguration des [Devcontainer](.devcontainer/devcontainer.json) und [Dockerfile](.devcontainer/Dockerfile) sind bereits vorhanden.

### Docker-Runner

Um diese Lösung zu nutzen, muss in der [Workspacekonfiguration](.vscode/settings.json) der Key `latex-workshop.docker.enabled: true` gesetzt werden.
