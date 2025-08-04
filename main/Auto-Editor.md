# [Auto-Editor](https://github.com/WyattBlue/auto-editor): Guia de Uso

## Descrição

O `auto-editor` é uma ferramenta de edição automática de vídeo e áudio que realiza cortes com base no silêncio ou nas faixas de áudio. Ele permite ajustar vídeos automaticamente, removendo partes que não têm som ou seguindo outras condições.

Este guia fornecerá exemplos e explicações sobre como utilizar o `auto-editor` para cortar faixas de áudio específicas, com foco na exportação para o formato de edição **Resolve**.

## Instalação

Antes de usar o `auto-editor`, você precisa instalá-lo. Se ainda não estiver instalado, siga os passos abaixo:

```bash
pip install auto-editor
```

Certifique-se de ter o `ffmpeg` instalado no seu sistema, pois o `auto-editor` depende dele para processar os arquivos de áudio e vídeo.

## Comandos Básicos

### 1. Cortar uma Faixa de Áudio

Para cortar uma única faixa de áudio de um vídeo, use o seguinte comando:

```bash
auto-editor video.mkv --edit audio:stream=0 --margin 0.2s --export resolve
```

#### Explicação:
- **video.mkv**: O arquivo de vídeo que você deseja editar.
- **--edit audio:stream=0**: Isso define que você deseja editar a faixa de áudio **0**. Lembre-se, as faixas de áudio começam a ser numeradas em **0**.
- **--margin 0.2s**: Adiciona uma margem de 0,2 segundos antes e depois de qualquer som detectado. Isso suaviza os cortes.
- **--export resolve**: Exporta o projeto no formato compatível com o DaVinci Resolve (um software de edição de vídeo).

### 2. Cortar Duas Faixas de Áudio ao Mesmo Tempo

Se o vídeo contém múltiplas faixas de áudio e você quer editar duas delas simultaneamente, use o seguinte comando:

```bash
auto-editor video.mkv --edit "(or audio:stream=1 audio:stream=2)" --margin 0.2s --export resolve
```

#### Explicação:
- **--edit "(or audio:stream=1 audio:stream=2)"**: Esse comando define que você quer editar tanto a faixa de áudio **1** quanto a faixa de áudio **2** ao mesmo tempo. A expressão entre parênteses significa "ou", permitindo que ambas as faixas sejam consideradas no processo de edição.
- O restante do comando segue a mesma lógica do exemplo anterior.

## Parâmetros Adicionais

- **--margin [tempo]**: Esse parâmetro define uma margem de tempo antes e depois de qualquer evento de áudio (som ou silêncio) para suavizar o corte. Exemplo: `--margin 0.5s` adiciona meio segundo de margem.
  
- **--export [formato]**: Define o formato de exportação final do vídeo. Alguns formatos comuns são:
  - **resolve**: Para exportar o projeto para o DaVinci Resolve.
  - **mp4**: Para exportar diretamente como um arquivo de vídeo MP4.

## Exemplo de Uso

Aqui está um exemplo completo para cortar faixas de áudio múltiplas e exportar para o DaVinci Resolve:

```bash
auto-editor video.mkv --edit "(or audio:stream=0 audio:stream=1)" --margin 0.3s --export resolve
```

Neste exemplo, o `auto-editor` irá considerar tanto a faixa de áudio **0** quanto a faixa **1**, cortando partes onde ambas as faixas estão em silêncio e adicionando uma margem de 0,3 segundos antes de cada som detectado.

---

### Explicação Adicional:

- **Stream**: As faixas de áudio em um vídeo são chamadas de "streams". O número da faixa **começa em 0**. Isso significa que a primeira faixa de áudio será referenciada como **audio:stream=0**, a segunda como **audio:stream=1**, e assim por diante.
  
- **Cortar uma faixa de áudio**: O primeiro exemplo faz cortes considerando apenas a primeira faixa de áudio do vídeo. Caso haja momentos de silêncio nesta faixa, eles serão removidos, e as partes com som serão mantidas.

- **Cortar duas faixas de áudio ao mesmo tempo**: No segundo exemplo, duas faixas de áudio são analisadas simultaneamente. Se ambas estiverem em silêncio ao mesmo tempo, o trecho correspondente será removido. A margem de 0,2 segundos é adicionada para suavizar os cortes e evitar interrupções bruscas.
