# Placa TK90X/95 revisão 6

## Instruções de montagem

A lista de componentes contém os componentes para a montagem da placa. Algums componentes não são necessários, explicados abaixo, e foram retirados na lista de componentes em excel mas listados nos arquivos TXT.

Utilize o arquivo PDF [mapa.pdf](mapa.pdf) para auxiliar na montagem.

Ao montar a placa, não é necessário soldar nada em `JP`, a PCB já vem com a conexão certa.

É possível usar soquetes nos CIs, a lista com quantidades está na versão em excel da lista de material. Para a ULA, caso use a versão clonada em CPLD, use soquete torneado para melhor encaixe.

Não montar os componentes `L1`, `L3`, `C41`, `R54`, `R57`, `R58`, `R59` e `D25_`

Se quiser ter 32K de RAM alta, montar `IC5`, `IC6`, `IC7`, `IC21`, `IC22`, `IC23`, `IC24`, `IC25`, `IC26`, `IC27` e não montar `D11`, `D12`, `R33`.

Caso queira somente 16KB de RAM baixa, não montar `IC5`, `IC6`, `IC7`, `IC21`, `IC22`, `IC23`, `IC24`, `IC25`, `IC26`, `IC27` e montar `D11`, `D12`, `R33`.

Nas memórias da RAM baixa, se for utilizar CIs 4116 feche o jumper `J2` para 12V e feche `J3`, se for utilizar CIs 4164 feche o jumper `J2` para 5V e não feche `J3`.

Se for usar a ROM (PROM) original, fechar o jumper `J1` no lado direito, se for usar EPROM (27C128) fechar jumper no lado esquerdo.

Na saída e entradas de K7 é possível fazer umas configurações de acordo com o tipo de conector utilizado:
 - No conector do EAR, se utilizar um jack P2 mono, feche o jumper `J5`, se for jack estéreo, feche `J5` somente se for utilizar cabo estéreo. Para jack estéreo e cabo mono não feche `J5`.
 - No conector do MIC utilize um jack estéreo e feche `J4` se quiser saída de áudio no canal esquerdo, ou deixe `J4` aberto para não ter saída de áudio. A saída de som K7 sai pelo canal direito.

Não esqueça de colocar um dissipador apropriado para o regulador 7805. É possível adaptar uma placa conversora de tensão DC/DC no lugar do 7805.

#### Relação de jumpers:

`JP` - fase de clock
`J1` - PROM/EPROM
`J2` - Alimentação 12V/5V para as DRAMs
`J3` - Alimentação -5V para as DRAMs
`J4` - Saída de áudio pelo conector MIC
`J5` - Jack EAR mono/estéreo

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
