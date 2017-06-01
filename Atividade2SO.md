
# Memória RAM
A memória RAM é um tipo de tecnologia que permite o acesso aos arquivos armazenados no computador. Diferentemente da memória do HD, a RAM não armazena conteúdos permanentemente. É responsável, no entanto, pela leitura dos conteúdos quando requeridos. Ou seja, de forma não-sequencial, por isso, a nomenclatura em inglês de Random Access Memory (Memória de Acesso Aleatório).
Para simplificar a lógica por trás da função da memória RAM, é possível fazer uma analogia com uma mesa de estudos, onde se reúne todo o material necessário para realizar os deveres de casa: como canetas, lápis, caderno e livros. Os materiais seriam os arquivos e a memória RAM, a mesa, onde tudo se reúne e o trabalho é feito.

Sendo assim, a memória RAM pode ser entendida como um espaço temporário de trabalho, pois, após a tarefa ser realizada, os arquivos (material de estudos) são retirados da memória (mesa) e mantidos no HD (armário).
Assim como a mesa, quanto maior a memória RAM, maior sua capacidade de trabalho. Mas a capacidade da mesa é medida em área. Quanto maior a área da mesa, mais livros cabem e mais rapidamente se faz o trabalho. Já a capacidade da memória RAM, mede-se pelo fluxo de bits suportados nas operações.

Ou seja, para se acessar uma grande quantidade de memória  no HD de uma só vez, como muitos programas atuais exigem, é necessário uma grande quantidade de memória RAM. São estes, portanto, os megabites ou gigabites que aparecem nas configurações.
A memória RAM é um chip semelhante a um micro-processador, composto por milhões de transistores e capacitores. O capacitor é uma peça capaz de armazenar elétrons. Quando ele está carregado, o sistema faz uma leitura com base no famoso código binário de “zeros e uns”. Cada leitura dessa em zero ou um significa um bit de informação. Essa leitura é feita de forma muito rápida, são muitas em poucos milésimos de segundos. É assim que a memória RAM processa todas as ações executadas pelo usuário.

# Memória ROM

A memória somente de leitura ou ROM (acrônimo em inglês de read-only memory) é um tipo de memória que permite apenas a leitura, ou seja, as suas informações são gravadas pelo fabricante uma única vez e após isso não podem ser alteradas ou apagadas, somente acessadas. São memórias cujo conteúdo é gravado permanentemente.[1]

Uma memória somente de leitura propriamente dita vem com seu conteúdo gravado durante a fabricação. Atualmente, o termo Memória ROM é usado informalmente para indicar uma gama de tipos de memória que são usadas apenas para a leitura na operação principal de dispositivos eletrônicos digitais, mas possivelmente podem ser escritas por meio de mecanismos especiais. Entre esses tipos encontramos as PROM, as EPROM, as EEPROM e as memórias flash. Ainda de forma mais ampla, e de certa forma imprópria, dispositivos de memória terciária, como CD-ROMs, DVD-ROMs, etc., também são algumas vezes citados como memória ROM.

Apesar do nome memória ROM ser usado algumas vezes em contraposição com o nome memória RAM, deve ficar claro que ambos os tipos de memória são de acesso aleatório.


# SWAP


No Linux, o swap é a memória virtual (também é conhecido como área de troca). A memória virtual funciona como uma extensão da memória RAM, que fica armazenada no disco. O porquê da memória swap precisar existir é simples: o sistema operacional precisa de memória para funcionar, e se a memória acabar, o sistema falha. O swap fica como uma reserva emergencial caso a memória RAM acabe. A memória swap era bastante útil em tempos passados onde memória RAM era algo mais escasso. Hoje em dia, tanto a RAM quanto espaço em disco estão baratos. É sempre recomendado utilizar swap, mesmo com muita memória RAM.

O swap pode ficar tanto em uma partição, quanto em um arquivo no disco. No caso de ficar numa partição em um disco comum (não-SSD), recomenda-se colocar a partição no início do disco, assim a leitura durante a rotação do disco magnético é mais rápida. No caso de partições em disco SSD, tanto faz pois não há rotações como um disco comum. Algumas distribuições, como Debian e Ubuntu, tem no instalador uma opção para colocar a partição no início do disco.

Importante: lembre-se que o swap é bem mais lento que a memória RAM. Se você colocar swap demais num sistema e começar a usá-lo muito você vai ganhar uma grande de uma lentidão! (muita lentidão em discos convencionais e mesmo assim lentidão em discos SSD)


### Que tamanho usar?

Desde os primórdios dos tempos, e você ainda vai encontrar muito essa informação, recomendava-se colocar sempre o dobro da RAM como swap. Por exemplo: se uma máquina tem 1GB de RAM, coloca-se 2GB de swap. Mas esse tipo de conselho era mais comum quando as máquinas tinham pouco de RAM. Se um servidor tem 16GB, geralmente não é necessário você colocar 32GB de swap.

Essa regra do dobro foi alterada mais recentemente. Se a máquina tem até 2GB de RAM, coloque o dobro. A partir daí, cada GB adicional de RAM é apenas RAM+2GB na swap. Ou seja:

* Um sistema de 2GB de RAM teria 4GB de swap (2×2).
* Um sistema de 3GB de RAM teria 5GB de swap (3+2).
* Um sistema de 8GB de RAM teria 10GB de swap (8+2).
* Um sistema de 16GB de RAM teria 18GB de swap (16+2).


# Paginação de Memória 

No contexto dos sistemas operacionais, a paginação da memória do computador é um processo de virtualização da memória que consiste na subdivisão da memória física em pequenas partições (frames), para permitir-lhe uma utilização mais eficiente. As frames da memória física correspondem a páginas de memória virtual. A alocação de memória é requisitada por páginas, a menor unidade deste método. Cada página é mapeada numa frame de memória através de um processo que chama paginação.

A paginação é implementada normalmente por unidades dedicadas de hardware integradas nos processadores. No caso dos processadores da família Intel x86, esta funcionalidade está atribuída à MMU. A paginação é obtida através de consulta a tabelas que relacionam os endereços lineares das páginas de memória com os endereços físicos das frames de memória respectivas.

Neste sistema, cada processo no computador tem a sua própria tabela de páginas, em que a cada endereço virtual corresponde o endereço físico em que a informação está efectivamente armazenada. Visto que a informação está dividida em pequenas unidades, o seu armazenamento não tem de ser necessariamente sequencial, o que elimina a fragmentação externa da memória.


