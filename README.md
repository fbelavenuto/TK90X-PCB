# TK90X-PCB

Recriação da placa de circuito impresso do microcomputador de 8 bits TK90X da Microdigital. Projeto iniciado em setembro de 2020.

## Agradecimentos

Agradecimentos ao Daniel Viana (Danjovic) pelo desenho do esquema no software Eagle, Manoel Carvalho (Neco) pelo encorajamento e scans limpos da PCB e ao grupo [Clube do TK](https://www.facebook.com/groups/clubedotk) do Facebook.

## Revisões

Nesse repositório existem várias revisões relacionadas abaixo, cada revisão contém modificações em relação à revisão anterior.

### Rev. 3

Réplica da placa Rev. 3 da Microdigital (Silk TK90X-B rev 3). Essa versão é para montagem de uma réplica da placa original, sem modificações.

### Rev. 4

As modificações efetuadas são:
- Jumpers de solda para selecionar o tipo de memória DRAM, roteando a alimentação corretamente,
- Jumper de solda para permitir o uso de uma EPROM no lugar da ROM original.

### Rev. 5

As modificações efetuadas são:
- Jumpers de solda nos conectores EAR e MIC para opção de montagem com Jacks P2 mono ou estéreo e saída de áudio no conector MIC
-  Desativação do circuito de RF dando lugar a uma saída de vídeo-composto on-board e conector RCA próprio.

Essa revisão não é encorajada a ser fabricada.

### Rev. 6

As modificações efetuadas são:
- Alteração no IC10 para corrigir a leitura da porta 254, compatibilizando esta porta com o padrão ZX e permitindo a execução de mais softwares.

Alguns componentes não precisam ser montados pela extinção do circuito de RF, veja a documentação específica na pasta *Docs* da revisão.

### Rev. 7

As modificações efetuadas são:
- Alteração nos componentes do circuito de vídeo:
  - Retirados os componentes não necessários referente ao circuito de RF,
  - IC12 foi rotacionado para abrir espaço para um conector RCA extra.
- Adicionado conectores dupont/pinheader:
  - Botão de RESET externo,
  - Chave para seleção de frequência vertical da ULA,
  - LED para uso no gabinete do TK95.
- Jumper de solda para seleção do tipo de sinal de vídeo a ser codificado (NTSC ou PAL/PAL-M) de acordo com o valor de cristal escolhido.
- Jumper de solda para permitir a ligação do sinal necessário para uso da interface [TK-MEM 128K](http://www.luccas.com.br/index.php/8-bits/artigos/23-preparando-o-tk90x-tk95-para-a-tkmem-128).

O conector RCA extra está posicionado no mesmo lugar da saída de RF do ZX Spectrum original, permitindo a montagem da placa dentro do seu gabinete original. Este conector extra é configurado por um jumper de solda que permite mapear o sinal de vídeo ou o sinal de áudio dando a opção de colocar um segundo RCA adaptando o case de um TK90X e ter saída de áudio em RCA.

# Pastas

*Common* possui arquivos referentes a todas as revisões.

Dentro de cada pasta de cada revisão há três subpastas com os nomes *Docs*, *Eagle* e *Gerber*. O esquema elétrico em PDF, imagens, lista de materiais, etc, estão em *Docs*. Na subpasta *Eagle* há os arquivos originais para a versão 9 do software Autodesk Eagle. Para a confecção das placas há os arquivos em formato gerber na pasta *Gerber* que podem ser enviados para uma empresa de fabricação de PCBs.

# Observações

É encorajado a fabricação da Rev. 7 por conter mais opções de configuração e correções de problemas conhecidos.

É recomendado a fabricação com finalização ENIG ou ouro no conector Edge para mais durabilidade.
