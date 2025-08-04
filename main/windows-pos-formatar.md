# Configuração Inicial do Windows

Se o seu computador já está formatado, siga estas etapas para deixar o Windows mais rápido, organizado e pronto para uso:

---

## ETAPA 1: Ativação do Windows e Office

### Opção 1: Método Seguro e Manual
- Siga este guia para ativar o Windows (8, 8.1, 10 ou 11 Pro) de graça:  
  [Activate Windows 8, 8.1, 10 and 11 Pro for Free](https://gist.github.com/Minionguyjpro/d913b3931e844ad8ad9a758a4aca4b63)

### Opção 2: Script Automático (Feito por Brasileiro)
- Créditos: Marcos Franco | Canal [Engenharia0800](https://www.youtube.com/@engenharia0800)

1. Primeiro, verifique se há atualizações no Windows:
   - Vá em `Configurações > Windows Update` e instale tudo o que aparecer. Reinicie o computador se necessário até que todas as atualizações estejam concluídas.
   
2. Abra o **PowerShell como administrador**:
   - Clique no botão Iniciar, digite "PowerShell", clique com o botão direito e selecione "Executar como administrador".
   
3. Digite este comando e pressione Enter:
   ```bash
   irm https://massgrave.dev/get | iex
   ```
   
4. Siga as instruções na tela:
   - Escolha `[1] WHID | Windows | Permanent` para ativar o Windows permanentemente.
   - Pressione Enter ou qualquer tecla para continuar.
   - Escolha `[2] Ohook | Office | Permanent` para ativar o Office.
   - Se precisar baixar o Office, selecione `[3] Download Office` e use este link:  
     [Download do Office - Microsoft 365 Offline](https://gravesoft.dev/download_windows_office/office_c2r_links/#portuguese-brazil-pt-br)
   - Após baixar, instale o Office normalmente.
   - Volte ao script e escolha `[1] Install Ohook Office Activation` para ativar.

5. (Opcional) Para otimizar o Windows:
   - No PowerShell como administrador, digite:
     ```bash
     irm https://christitus.com/win | iex
     ```
   - Isso instala uma ferramenta útil para ajustes e remoção de bloatware. Veja mais em: [One Tool for Everything](https://christitus.com/one-tool-for-everything/).

---

## ETAPA 2: Preparando o Sistema
Antes de instalar programas, instale os pacotes Visual C++, que são essenciais para o funcionamento de muitos aplicativos:

1. Baixe o arquivo `VisualCppRedist_AIO_x86_x64_82.zip` (ou a versão mais recente) aqui:  
   [Visual C++ 2022 Redistributable](https://github.com/abbodi1406/vcredist/releases)
2. Extraia o arquivo e execute o instalador.
3. Se o antivírus reclamar, ignore o aviso — o arquivo é seguro.

---

## ETAPA 3: Atualizando e Instalando Programas com Winget
O `winget` é uma ferramenta nativa do Windows que facilita instalar e atualizar programas de forma rápida.

1. Abra o **Prompt de Comando** ou **PowerShell** como administrador.
2. Atualize todos os programas já instalados:
   ```bash
   winget update --all
   ```
   ```bash
   winget upgrade --all
   ```
3. Pesquise um programa:
   ```bash
   winget search [nome do programa]
   ```
4. Instale um programa:
   ```bash
   winget install [nome do programa]
   ```

---

## Ativando o "GodMode" no Windows
O "GodMode" é um atalho que reúne várias configurações avançadas do Windows em uma única pasta. Veja como ativar:

1. Crie uma nova pasta em qualquer lugar (como na Área de Trabalho).
2. Renomeie a pasta para:
   ```bash
   GodMode.{ED7BA470-8E54-465E-825C-99712043E01C}
   ```
3. Pressione Enter. A pasta mudará de ícone e, ao abri-la, você verá várias opções avançadas do sistema.

---

# PROGRAMAS ESSENCIAIS

## Programas Obrigatórios para Arquivos
1. [TeraCopy](https://www.codesector.com/teracopy) - Transfere arquivos mais rápido e com segurança.
2. [7-Zip](https://www.7-zip.org/) - Descompacta e compacta arquivos de forma simples e gratuita.
3. [WinRAR](https://www.win-rar.com/) - Outra opção popular para gerenciar arquivos compactados.

## Navegadores
Aqui está uma lista de navegadores que rodam em computadores (Windows, macOS ou Linux), com destaque para os mais seguros:

1. [Avast Secure Browser](https://www.avast.com/secure-browser) - Navegador com VPN e bloqueio de anúncios.
2. [Baidu Browser](https://browser.baidu.com/) - Baseado em Chromium, rápido, mas coleta dados.
3. [Brave](https://brave.com/) - **Seguro**: Bloqueia anúncios e rastreadores, foca em privacidade.
4. [Bromite](https://www.bromite.org/) - **Seguro**: Chromium com privacidade reforçada (disponível via compilação ou sideload).
5. [Chromium](https://www.chromium.org/) - Base aberta do Chrome, menos rastreamento que o original.
6. [Comodo Dragon](https://www.comodo.com/home/browsers-toolbars/browser.php) - Baseado em Chromium, com foco em segurança.
7. [Epic Privacy Browser](https://www.epicbrowser.com/) - **Seguro**: Bloqueia rastreadores e usa proxy criptografado.
8. [Firefox](https://www.mozilla.org/firefox/) - **Seguro**: Open-source, com opções de privacidade ajustáveis.
9. [GNU IceCat](https://www.gnu.org/software/icecat/) - **Seguro**: Fork do Firefox, totalmente livre e privado.
10. [Google Chrome](https://www.google.com/chrome/) - Navegador mais popular, mas coleta muitos dados.
11. [Iridium](https://iridiumbrowser.de/) - **Seguro**: Baseado em Chromium, com privacidade reforçada.
12. [LibreWolf](https://librewolf.net/) - **Seguro**: Fork do Firefox com privacidade extrema.
13. [Maxthon](https://www.maxthon.com/) - Navegador leve com recursos extras.
14. [Microsoft Edge](https://www.microsoft.com/edge) - Baseado em Chromium, com boas opções de segurança.
15. [Midori](https://astian.org/midori/) - Navegador leve, segurança básica.
16. [Norton Private Browser](https://www.norton.com/products/norton-private-browser) - **Seguro**: Focado em proteção antivírus e privacidade.
17. [Opera](https://www.opera.com/) - Inclui VPN grátis e bloqueador de anúncios.
18. [Pale Moon](https://www.palemoon.org/) - **Seguro**: Fork do Firefox, leve e privado.
19. [Safari](https://www.apple.com/safari/) - **Seguro**: Navegador da Apple com proteção contra rastreamento (disponível via macOS ou emuladores).
20. [Samsung Internet](https://www.samsung.com/br/apps/samsung-internet/) - Disponível para Windows via emuladores Android.
21. [SeaMonkey](https://www.seamonkey-project.org/) - Suíte de internet com navegador básico.
22. [Tor Browser](https://www.torproject.org/) - **Seguro**: Usa rede Tor para anonimato total.
23. [UC Browser](https://www.ucweb.com/) - Popular na Ásia, mas com preocupações de privacidade.
24. [Ulaa](https://ulaa.com/) - Navegador novo com foco em produtividade e segurança.
25. [Vivaldi](https://vivaldi.com/) - **Seguro**: Personalizável, com bloqueio de rastreadores.
26. [Waterfox](https://www.waterfox.net/) - **Seguro**: Fork do Firefox focado em privacidade.
27. [Yandex Browser](https://browser.yandex.com/) - Baseado em Chromium, mas coleta dados.

**Nota**: Os navegadores marcados como **Seguro** são ideais para quem prioriza privacidade e segurança.

## Comunicação e Colaboração
1. [Discord](https://discord.com/) - Chat para jogos, estudo ou trabalho.
2. [Zoom](https://zoom.us/) - Videochamadas para reuniões ou amigos.
3. [Microsoft Teams](https://www.microsoft.com/pt-br/microsoft-teams/) - Colaboração em equipe.
4. [Slack](https://slack.com/) - Comunicação profissional para equipes.

## Multimídia
1. [VLC Media Player](https://www.videolan.org/vlc/) - Reproduz qualquer formato de vídeo ou áudio.
2. [Spotify](https://www.spotify.com/br-pt/) - Streaming de músicas e podcasts.
3. [Audacity](https://www.audacityteam.org/) - Edição de áudio gratuita.
4. [OBS Studio](https://obsproject.com/) - Gravação e transmissão de vídeos.

## Editores de Texto (Foco em Programação)
1. [Visual Studio Code](https://code.visualstudio.com/) - Editor leve e popular para programar em várias linguagens.
2. [Notepad++](https://notepad-plus-plus.org/) - Editor simples e rápido para códigos e arquivos grandes.
3. [Vim](https://www.vim.org/) - Editor poderoso baseado em terminal, ideal para servidores.
4. [Neovim](https://neovim.io/) - Versão moderna do Vim com mais recursos e personalização.
5. [Sublime Text](https://www.sublimetext.com/) - Editor rápido com interface minimalista.
6. [Atom](https://atom.io/) - Editor personalizável, ótimo para colaboração.
7. [Emacs](https://www.gnu.org/software/emacs/) - Editor configurável baseado em terminal, muito versátil.
8. [Nano](https://www.nano-editor.org/) - Editor simples para terminal, fácil para iniciantes.
9. [Brackets](http://brackets.io/) - Editor leve focado em desenvolvimento web.
10. [Geany](https://www.geany.org/) - Editor rápido com recursos de mini-IDE.

## Ferramentas de Desenvolvimento
1. [Git](https://git-scm.com/) - Controle de versão essencial para programadores.
2. [GitHub Desktop](https://desktop.github.com/) - Interface gráfica para usar o Git.
3. [Node.js](https://nodejs.org/) - Ambiente para rodar JavaScript fora do navegador.
4. [Python](https://www.python.org/) - Linguagem de programação versátil e fácil de aprender.
5. [Docker](https://www.docker.com/) - Criação e execução de contêineres.

## IDEs (Ambientes de Desenvolvimento Integrados)
1. [Android Studio](https://developer.android.com/studio) - IDE oficial para desenvolvimento Android.
2. [Arduino IDE](https://www.arduino.cc/en/software) - Desenvolvimento para placas Arduino.
3. [CLion](https://www.jetbrains.com/clion/) - IDE para C e C++ da JetBrains.
4. [Code::Blocks](http://www.codeblocks.org/) - IDE leve para C, C++ e Fortran.
5. [Delphi](https://www.embarcadero.com/products/delphi) - IDE para Pascal/Object Pascal, ótimo para aplicativos desktop.
6. [Eclipse](https://www.eclipse.org/) - IDE popular para Java, mas suporta várias linguagens.
7. [IntelliJ IDEA](https://www.jetbrains.com/idea/) - IDE robusta para Java e outras linguagens.
8. [Lazarus](https://www.lazarus-ide.org/) - IDE gratuita para Pascal, alternativa ao Delphi.
9. [NetBeans](https://netbeans.apache.org/) - IDE para Java, PHP, HTML5 e mais.
10. [PHPStorm](https://www.jetbrains.com/phpstorm/) - IDE especializada em PHP.
11. [PyCharm](https://www.jetbrains.com/pycharm/) - IDE completa para Python.
12. [Qt Creator](https://www.qt.io/product/development-tools) - IDE para C++ e desenvolvimento com Qt.
13. [Rider](https://www.jetbrains.com/rider/) - IDE para C# e .NET da JetBrains.
14. [RubyMine](https://www.jetbrains.com/rubymine/) - IDE para Ruby e Rails.
15. [RustRover](https://www.jetbrains.com/rust/) - IDE para Rust da JetBrains.
16. [Visual Studio](https://visualstudio.microsoft.com/) - IDE profissional da Microsoft para C#, C++, Python e mais.
17. [Visual Studio Community](https://visualstudio.microsoft.com/vs/community/) - Versão gratuita do Visual Studio.
18. [WebStorm](https://www.jetbrains.com/webstorm/) - IDE para JavaScript, HTML e CSS.
19. [Xcode](https://developer.apple.com/xcode/) - IDE para Swift e Objective-C (macOS ou emuladores).
20. [Dev-C++](https://www.bloodshed.net/) - IDE simples para C e C++.

## Drivers e Componentes Essenciais
1. [NVIDIA GeForce Drivers](https://www.nvidia.com/Download/index.aspx) - Drivers para placas de vídeo NVIDIA (GeForce, RTX).
2. [AMD Radeon Software](https://www.amd.com/en/support) - Drivers para placas de vídeo AMD (Radeon, RX).
3. [Intel Graphics Drivers](https://www.intel.com/content/www/us/en/support/detect.html) - Drivers para gráficos integrados Intel (HD, UHD, Iris).
4. [DirectX Runtime](https://www.microsoft.com/en-us/download/details.aspx?id=35) - Biblioteca essencial para jogos e gráficos 3D.
5. [Vulkan Runtime](https://vulkan.lunarg.com/) - API moderna para gráficos, usada em jogos recentes.
6. [OpenGL Drivers](https://www.opengl.org/) - Drivers para suporte a gráficos OpenGL (geralmente incluídos com drivers de placa).
7. [Driver Booster](https://www.iobit.com/pt/driver-booster.php) - Ferramenta para atualizar todos os drivers automaticamente.

## Controle Remoto
1. [AnyDesk](https://anydesk.com/pt) - Acesso remoto rápido e leve.
2. [TeamViewer](https://www.teamviewer.com/pt-br/) - Ferramenta popular para suporte remoto.
3. [RustDesk](https://rustdesk.com/) - Alternativa gratuita e open-source para acesso remoto.
4. [Chrome Remote Desktop](https://remotedesktop.google.com/) - Controle remoto simples via navegador Chrome.
5. [Microsoft Remote Desktop](https://learn.microsoft.com/pt-br/windows-server/remote/remote-desktop-services/clients/remote-desktop-clients) - Ferramenta nativa do Windows para acesso remoto.

## Produtividade
1. [Notion](https://www.notion.so/) - Organização de tarefas, notas e projetos.
2. [Microsoft Office](https://www.microsoft.com/pt-br/microsoft-365) - Word, Excel e PowerPoint.
3. [LibreOffice](https://pt-br.libreoffice.org/) - Alternativa gratuita ao Office.
4. [Todoist](https://todoist.com/) - Gerenciamento de tarefas simples.
5. [KDE Connect](https://kdeconnect.kde.org/) - Conecta seu PC ao celular para compartilhar arquivos e notificações.

## Edição de Imagens

### Edição 2D
1. [GIMP](https://www.gimp.org/) - Editor de imagens gratuito, similar ao Photoshop.
2. [Photopea](https://www.photopea.com/) - Editor de imagens online, sem necessidade de instalação.
3. [Photoshop](https://www.adobe.com/products/photoshop.html) - Editor de imagens profissional (pago).
4. [Paint.NET](https://www.getpaint.net/) - Editor de imagens leve e gratuito.
5. [Krita](https://krita.org/) - Editor gratuito para desenho digital e pintura.

### Edição e Modelagem 3D
1. [Blender](https://www.blender.org/) - Software gratuito para modelagem, animação e renderização 3D.
2. [Autodesk Maya](https://www.autodesk.com/products/maya/overview) - Software profissional para animação e modelagem 3D (pago).
3. [3ds Max](https://www.autodesk.com/products/3ds-max/overview) - Ferramenta profissional para modelagem e renderização 3D (pago).
4. [Cinema 4D](https://www.maxon.net/en/cinema-4d) - Software 3D para animação e motion graphics (pago).
5. [ZBrush](https://www.maxon.net/en/zbrush) - Ferramenta para escultura digital 3D (pago).
6. [SketchUp](https://www.sketchup.com/) - Modelagem 3D simples, ótimo para arquitetura (versão gratuita e paga).
7. [FreeCAD](https://www.freecad.org/) - Software gratuito e open-source para design 3D e CAD.
8. [Tinkercad](https://www.tinkercad.com/) - Ferramenta 3D online e gratuita, ideal para iniciantes.
9. [Fusion 360](https://www.autodesk.com/products/fusion-360/overview) - Software 3D para design e engenharia (grátis para uso pessoal).
10. [Houdini](https://www.sidefx.com/products/houdini/) - Ferramenta avançada para efeitos 3D e simulações (versão gratuita limitada).
11. [Daz 3D](https://www.daz3d.com/) - Software gratuito para criação de personagens 3D.

## Editores de Vídeo
1. [DaVinci Resolve](https://www.blackmagicdesign.com/products/davinciresolve/) - Edição de vídeo profissional gratuita.
2. [Shotcut](https://shotcut.org/) - Editor de vídeo leve e fácil de usar.
3. [Adobe Premiere Pro](https://www.adobe.com/products/premiere.html) - Editor de vídeo profissional (pago).
4. [Filmora](https://filmora.wondershare.com/) - Editor de vídeo simples e acessível.
5. [Vegas Pro](https://www.vegascreativesoftware.com/br/vegas-pro/) - Editor de vídeo profissional (pago).
6. [OpenShot](https://www.openshot.org/) - Editor de vídeo gratuito e open-source.
7. [HitFilm Express](https://fxhome.com/product/hitfilm) - Editor de vídeo gratuito com efeitos visuais.
8. [Kdenlive](https://kdenlive.org/en/) - Editor de vídeo gratuito e open-source, poderoso e leve.

## Produção Musical
1. [FL Studio](https://www.image-line.com/) - DAW popular para produção musical (pago).
2. [Ableton Live](https://www.ableton.com/) - DAW profissional para composição e apresentações (pago).
3. [Reaper](https://www.reaper.fm/) - DAW acessível e personalizável (teste grátis, licença barata).
4. [LMMS](https://lmms.io/) - DAW gratuita e open-source, similar ao FL Studio.
5. [Cakewalk](https://www.bandlab.com/products/cakewalk) - DAW gratuita para produção musical.
6. [Ardour](https://ardour.org/) - DAW open-source para gravação e mixagem.
7. [MuseScore](https://musescore.org/) - Software gratuito para composição e partituras.

## Segurança
1. [KeePassXC](https://keepassxc.org/) - Gerenciador de senhas seguro e offline.
2. [Bitwarden](https://bitwarden.com/) - Gerenciador de senhas gratuito e sincronizado na nuvem.

## Jogos
1. [Steam](https://store.steampowered.com/) - Plataforma de jogos mais popular.
2. [Epic Games Store](https://www.epicgames.com/store/) - Jogos grátis toda semana.
3. [GOG Galaxy](https://www.gog.com/galaxy) - Jogos sem DRM.
4. [Ubisoft Connect](https://www.ubisoft.com/pt-br/game/ubisoft-connect) - Plataforma para jogos da Ubisoft.
5. [EA App](https://www.ea.com/pt-br/ea-app) - Plataforma para jogos da Electronic Arts (substitui Origin).
6. [Rockstar Games Launcher](https://www.rockstargames.com/rockstargameslauncher) - Launcher para jogos da Rockstar.
7. [Battle.net](https://www.blizzard.com/pt-br/apps/battle.net/desktop) - Plataforma para jogos da Blizzard.
8. [Itch.io](https://itch.io/) - Plataforma para jogos independentes.
9. [MSI Afterburner](https://www.msi.com/Landing/afterburner) - Ferramenta para overclock e monitoramento de GPU.
10. [Rivatuner Statistics Server](https://www.guru3d.com/content-page/rivatuner.html) - Mostra FPS e desempenho em jogos.

---

# Removendo Propagandas do WinRAR

1. Baixe e instale o [WinRAR](https://www.win-rar.com/).
2. Crie um arquivo de texto vazio (clique com o botão direito > Novo > Documento de Texto).
3. Copie e cole este conteúdo no arquivo:
   ```text
   RAR registration data
   SiM
   Local Site License
   UID=ca5575bd41c33ec5a2de
   6412212250a2de7c818d537f99bcf0218861216f4ce0738e2ef7ad
   8bc2514534357f5541ed60694c88f20734f7fa6ad968865654a57b
   0f0edf295d607ce6fa6d6b3667401b413bdcbccca3152c8ab6abc5
   931818a35674a26f065261f8bce32dfbce601d1aa079a3c54f79c7
   adeacb886214457e000e50d6ff5329a2f516ebba72708a35f704db
   3d30b1633de64c1bdc0c5c2b54710967dde4c9aab721b69460185e
   a12e2906a44bc32601e8ef0028d453a1d8b40dd23b562696892555
   ```
4. Vá em `Arquivo > Salvar Como`:
   - Escolha o local: `C:\Program Files\WinRAR`.
   - Mude "Tipo" para `Todos os Arquivos (*.*)`.
   - Nomeie como `rarreg.key` e salve.
5. Pronto! As propagandas sumirão.

---

# Reparando o Windows com 3 Comandos
Se o sistema estiver lento ou com problemas, use estes comandos no **PowerShell como administrador**:

1. ```bash
   chkdsk /f
   ```
   - Corrige erros no disco rígido.
   
2. ```bash
   chkdsk /r
   ```
   - Encontra e tenta recuperar setores defeituosos no disco.
   
3. ```bash
   DISM /Online /Cleanup-image /Restorehealth
   ```
   - Verifica e repara arquivos do sistema corrompidos.

---

# Antivírus Gratuitos
1. [ESET Online Scanner](https://www.eset.com/) - Verificação online rápida.
2. [Kaspersky Virus Removal Tool](https://www.kaspersky.com/downloads/free-virus-removal-tool) - Remove ameaças específicas.
3. [Malwarebytes](https://br.malwarebytes.com) - Proteção contra malwares.
4. [Windows Defender](https://www.microsoft.com/pt-br/windows/comprehensive-security) - Antivírus embutido no Windows, simples e eficiente.

---

# Dicas Pós-Formatação do Windows

1. **Desative Programas na Inicialização**:
   - Pressione `Ctrl + Shift + Esc` para abrir o Gerenciador de Tarefas.
   - Vá na aba `Inicializar` e desative programas desnecessários para acelerar a inicialização.

2. **Ajuste o Desempenho Visual**:
   - Pesquise `Ajustar a aparência e o desempenho do Windows` no menu Iniciar.
   - Escolha `Ajustar para melhor desempenho` ou personalize as opções.

3. **Instale Drivers Atualizados**:
   - Use o site do fabricante da sua placa-mãe, GPU ou notebook para baixar drivers (ex.: NVIDIA, AMD, Intel).
   - Ou instale [Driver Booster](https://www.iobit.com/pt/driver-booster.php) para facilitar.

4. **Faça Backup Regularmente**:
   - Use o `Histórico de Arquivos` do Windows (busque em Configurações) ou ferramentas como [Macrium Reflect](https://www.macrium.com/reflectfree).

5. **Remova Bloatware Pré-Instalado**:
   - Use o script do Chris Titus (mencionado na ETAPA 1) ou desinstale manualmente em `Configurações > Aplicativos`.

6. **Habilite a Proteção do Sistema**:
   - Pesquise `Criar um ponto de restauração` no menu Iniciar e ative a proteção para a unidade C:.

7. **Personalize a Barra de Tarefas**:
   - Clique com o botão direito na barra e ajuste ícones, posição ou remova a busca do Cortana.
