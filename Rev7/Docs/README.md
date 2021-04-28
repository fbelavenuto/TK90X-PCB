# Placa TK90X/95 revisão 7

## Instruções de montagem

A lista de componentes contém os componentes para a montagem da placa. Algums componentes são opcionais, explicado no texto. A lista não contempla chaves e botões opcionais relatados no texto.

Utilize o arquivo PDF [mapa.pdf](mapa.pdf) para auxiliar na montagem.

Ao montar a placa, não é necessário soldar nada em `JP`, a PCB já vem com a conexão certa.

No conector de energia `X1` existe o jumper `J1` para configurar o tipo de jack usado. Feche `J1` para jack P2 mono ou deixe aberto para jack P2 estéreo.

Se quiser ter 32K de RAM alta, montar `IC5`, `IC6`, `IC7`, `IC21`, `IC22`, `IC23`, `IC24`, `IC25`, `IC26`, `IC27` e não montar `D11`, `D12`, `R33`.

Caso queira somente 16KB de RAM baixa, não montar `IC5`, `IC6`, `IC7`, `IC21`, `IC22`, `IC23`, `IC24`, `IC25`, `IC26`, `IC27` e montar `D11`, `D12`, `R33`.

Nas memórias da RAM baixa, se for utilizar CIs 4116 feche o jumper `J2` para 12V e feche `J3`, se for utilizar CIs 4164 feche o jumper `J2` para 5V e não feche `J3`.

Se for usar a ROM (PROM) original, fechar o jumper `J9` no lado `R`, se for usar EPROM (27C128) fechar jumper no lado `E`.

O jumper `J10` se aberto configura a ULA para trabalhar em 60Hz de sincronismo vertical. Se fechá-lo a ULA é configurada para 50Hz. Pode ser utilizado uma chave externa para esta função.

É possível escolher o padrão de vídeo PAL-M ou NTSC. Para PAL-M utilize um cristal de 14.3044 MHz e feche o jumper `J7` para PAL. NTSC utilize cristal de 14.318MHz e feche `J7` para NTSC.

Na saída e entradas de K7 é possível fazer umas configurações de acordo com o tipo de conector utilizado:
 - No conector do EAR, se utilizar um jack P2 mono, feche o jumper `J5`, se for jack estéreo, feche `J5` somente se for utilizar cabo estéreo. Para jack estéreo e cabo mono não feche `J5`.
 - No conector do MIC utilize um jack estéreo e feche `J4` se quiser saída de áudio no canal esquerdo, ou deixe `J4` aberto para não ter saída de áudio. A saída de som K7 sai pelo canal direito.

A saída de vídeo está ligada no conector RCA `X4`, é possível soldar um conector RCA em `X5` e pelo jumper `J8` escolher que sinal estará presente nesse conector:
 - Se for montar para gabinete ZX não solde `X4`, solde `X5` e configure `J8` para vídeo.
 - Caso queira furar o gabinete do TK90X e ter uma saída de áudio em RCA, solde também `X5` e configure `J8` para áudio.

`X7` é o conector de joystick, solde-o para gabinete TK90X e não o solde para gabinete ZX caso não queira furar o gabinete.

Outra opção deixada é a conexão para a interface TKMEM. Feche `J6` caso queira ligar o barramento ao circuito responsável por desligar a RAM alta ao conectar a TKMEM.

Caso deseje colocar um push-button externo para RESET, ligue-o ao conector `X8`.

Não esqueça de colocar um dissipador apropriado para o regulador 7805. É possível adaptar uma placa conversora de tensão DC/DC no lugar do 7805.

#### Relação de jumpers:

`JP` - fase de clock
`J1` - Jack power mono/estéreo
`J2` - Alimentação 12V/5V para as DRAMs
`J3` - Alimentação -5V para as DRAMs
`J4` - Saída de áudio pelo conector MIC
`J5` - Jack EAR mono/estéreo
`J6` - Opção TK-MEM
`J7` - NTSC/PAL
`J8` - Vídeo/áudio em X5
`J9` - ROM/EPROM
`J10` - ULA 50/60 Hz

#### Relação de test points:

`TP1` - Clock Z80
`TP2` - Clock ULA
`TP3` - Entrada K7
`TP4` - DRAM /RAS
`TP5` - DRAM /CAS
`TP6` - DRAM /WR
`TP7` - Saída Beep ULA
`TP8` - Sincronismo composto
`TP9` - /ROM select
`TP10` - /IRQ

## Fotos

Segue exemplo de montagem. Nesta montagem de validação foram testados todas as opções. Foi utilizado uma placa DC/DC no lugar do 7805, DRAMs 4416 e EPROM. Não foi soldado um conector em `X5`, os jacks do MIC e EAR são estéreos e o Jack `X1` é mono. Foi utilizado nos testes uma ULA original e um clone em FPGA, que aparece nas fotos.


![Lado dos componentes](Foto_Montada_Top.jpg)
*Lado dos componentes*


![Lado da solda](Foto_Montada_Bottom.jpg)
*Lado da Solda*
