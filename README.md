# TK90X-PCB

Recriação da placa de circuito impresso do microcomputador de 8 bits TK90X da Microdigital.

Recriado em setembro de 2020.

Agradecimentos ao @Danjovic pelo esquema inicial, Manoel Carvalho (Neco) pelo encorajamento e scans limpos da PCB e ao grupo [Clube do TK](https://www.facebook.com/groups/clubedotk) do FB.

Nesse repositório existem várias revisões explicadas abaixo, cada revisão contém modificações em relação à revisão anterior:

- **Rev. 3**, réplica da placa Rev. 3 da Microdigital (Silk TK90X-B rev 3). Essa versão é para quem quiser ter uma réplica igual à placa original, sem modificações.
- **Rev. 4**, contém algumas modificações como jumpers de solda para selecionar o tipo de memória DRAM, roteando a alimentação corretamente, e um jumper de solda para permitir o uso de uma EPROM no lugar da ROM original.
- **Rev. 5**, contém a adição de jumpers de solda nos conectores EAR e MIC para opção de montagem com Jacks P2 mono ou estéreo e saída de áudio no conector MIC e a desativação do circuito de RF dando lugar a uma saída de vídeo-composto on-board e conector RCA próprio. Essa revisão não é encorajada a ser fabricada, use a Rev. 6
- **Rev. 6**, contém alteração no IC10 para corrigir a leitura da porta 254, compatibilizando esta porta com o padrão ZX e permitindo a execução de mais softwares. Alguns componentes não precisam ser montados pela extinção do circuito de RF, veja a documentação específica na pasta *Docs* da revisão.
- **Rev. 7**, contém alteração nos componentes do circuito de vídeo, foram retirados os componentes não necessários e o IC12 foi rotacionado para abrir espaço para um conector RCA extra. Esta revisão permite a solda de um segundo RCA posicionado no mesmo lugar da saída de RF do ZX Spectrum original, permitindo a montagem da placa dentro de um gabinete de ZX Spectrum. Este conector extra é configurado por um jumper de solda que permite mapear o sinal de vídeo ou o sinal de áudio, para a opção de colocar um segundo RCA adaptando o case de um TK90X e ter uma saída de áudio em RCA. Foi adicionado conectores dupont para uso de um botão de RESET externo, chave para seleção de frequência vertical da ULA e saída para LED para uso no gabinete do TK95. Há um jumper de solda para seleção do tipo de sinal de vídeo a ser codificado (NTSC ou PAL/PAL-M). Há também um jumper de solda para permitir a ligação do sinal necessário para uso da interface TK-MEM 128K.

Cada pasta de cada revisão há três subpastas com os nomes *Docs*, *Eagle* e *Gerber*. O esquema elétrico em PDF, imagens, lista de materiais, etc, estão em *Docs*. Na subpasta *Eagle* há os arquivos originais para a versão 9 do software Autodesk Eagle. Para a confecção das placas há os arquivos em formato gerber na pasta *Gerber* que podem ser enviados para uma empresa de fabricação de PCBs.

É encorajado a fabricação da Rev. 7 por conter mais opções de configuração e correções de problemas conhecidos. É recomendado a fabricação com finalização ENIG ou ouro no conector Edge para mais durabilidade.
