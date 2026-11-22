MAG-TV v2 - skin para Enigma2 (OpenATV 6.x), 1280x720
====================================================

Mesmo aspeto do e2player / TVH Player:
  - Lista de canais com pre-visualizacao do video, picon, programa atual,
    progresso, "a seguir" e descricao do canal selecionado.
  - Barra de informacao com numero, picon, nome, agora / a seguir, progresso,
    minutos que faltam e relogio (fundo 30% transparente).
  - Segunda barra (INFO duas vezes) com a descricao completa.
  - Restantes janelas (menus, configuracoes, EPG...) com a mesma paleta de cores.

CONTEUDO
  usr/share/enigma2/MAG-TV/                  skin, letras (DejaVu) e molduras
  usr/lib/enigma2/python/Components/Converter/MagInfo.py
                                             conversor do skin (numero do canal,
                                             horario, minutos restantes, a seguir)

INSTALACAO (por SSH/Telnet, ex. PuTTY)
  1. Copia o ficheiro mag-tv-skin.tar.gz para /tmp da box (FTP, utilizador root).
  2. Na box:
        tar -xzf /tmp/mag-tv-skin.tar.gz -C /
  3. Menu > Configuracao > Sistema > Skin (Interface de utilizador) > escolhe "MAG-TV"
     e aceita reiniciar a interface.

  Sem SSH: copia por FTP as pastas  usr/share/enigma2/MAG-TV  e o ficheiro
  MagInfo.py para os mesmos caminhos na box, e depois escolhe o skin no menu.

SE A INTERFACE NAO ARRANCAR (recuperacao, por SSH/Telnet)
        init 4
        sed -i '/config.skin.primary_skin/d' /etc/enigma2/settings
        init 3
  A box volta ao skin original.

PERSONALIZAR
  - Transparencia da barra de informacao: em skin.xml, cor "ib_bg"
    (#00131924 opaca, #33... 20%, #4d... 30%, #66... 40%, #80... 50%).
  - Numero de canais visiveis na lista: serviceItemHeight (40 = 16 linhas).

LIMITACOES
  - A lista de grupos (bouquets) nao fica sempre visivel ao lado dos canais como na
    app: no Enigma2 a lista de bouquets abre-se com a tecla de bouquets/esquerda.
  - A barra de progresso dentro da lista segue a opcao do OpenATV
    "mostrar progresso do evento na lista de canais".
