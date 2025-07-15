# Desenvolvimento de um Pedal de Efeito Fuzz para Guitarra Baseado em Circuitos Analógicos

## Introdução

Desenvolver uma pedal de efeito fuzz para guitarra baseada em circuitos analógicos. O projeto visa explorar diferentes configurações eletrônicas para a modulação do sinal da guitarra, procurando explorar as diferentes topologias que podem ser aplicadas para fornecer o efeito desejado, afim de decidir qual topologia é a mais fácil de ser aplicada, garantindo um efeito coerente e que pode ser utilizado para fins de aprendizado.

## Revisão da literatura

O pedal fuzz é um dos efeitos mais emblemáticos e transformadores na história da guitarra elétrica, imediatamente reconhecível por seu som distorcido e granulado. Sua origem remonta a falhas técnicas e experimentações acidentais que ocorreram no início dos anos 1950 e 1960. Um exemplo seminal é a gravação de "Rocket 88" por Ike Turner & His Kings of Rhythm em 1951, onde um amplificador de guitarra danificado produziu uma distorção acidental que se tornou um marco sonoro. Similarmente, em 1961, na gravação de "Don't Worry" de Marty Robbins, o engenheiro de som Grady Martin utilizou um pré-amplificador defeituoso para criar um solo de guitarra distorcido, demonstrando como acidentes podem catalisar novas explorações tonais.

Esses incidentes acidentais serviram como catalisadores para a busca intencional desse timbre particular. A demanda por uma replicação controlada do som distorcido impulsionou a inovação tecnológica no campo da eletrônica musical. O primeiro pedal comercial, o Maestro FZ-1 Fuzz-Tone, foi lançado pela Gibson em 1962. Embora as vendas iniciais fossem lentas, sua popularidade explodiu após o uso proeminente por Keith Richards dos Rolling Stones na icônica "(I Can't Get No) Satisfaction" em 1965, impulsionando o interesse e a demanda pelo efeito. Desde então, o fuzz moldou e influenciou profundamente diversos gêneros musicais, como rock psicodélico, hard rock, heavy metal, punk, shoegaze e grunge, tornando-se uma ferramenta essencial para a expressão criativa de guitarristas renomados como Jimi Hendrix, David Gilmour e Billy Corgan.   


<p align="center">
  Imagem 1: Pedal Maestro FZ-1 Fuzz-Tone
</p>
<p align="center">
  <img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/7fb38966-a41a-4ed4-8def-7394c5c4c5c1" />
</p>
<p align="center">
 Fonte: Google Imagens
</p>
Neste projeto serão explorados o histórico do efeito, os princípios eletrônicos subjacentes que governam sua operação, as topologias de circuito clássicas que definiram seu som, o papel específico de cada componente eletrônico, as características elétricas fundamentais para seu funcionamento e integração, as modificações comuns que permitem a personalização tonal e as técnicas de redução de ruído para otimizar o desempenho. O objetivo final é capacitar o construtor com o conhecimento aprofundado necessário para projetar, montar, testar e otimizar um pedal fuzz, compreendendo as nuances técnicas que definem seu timbre e desempenho no contexto de um trabalho acadêmico. O construtor deve reconhecer que as "imperfeições" do circuito (como o clipping severo) são, na verdade, a fonte do caráter único do fuzz. Além disso, a história destaca a importância da interação do pedal com outros elementos da cadeia de sinal (guitarra, amplificador) e o papel do músico na moldagem do som, incentivando a experimentação e a compreensão do sistema.   

### Primeiros Pedais Comerciais e Popularização

A crescente demanda por um dispositivo que pudesse reproduzir consistentemente esse som distorcido, sem depender de equipamentos defeituosos ou sobrecarregados, levou à invenção dos primeiros pedais fuzz dedicados. O Maestro Fuzz-Tone FZ-1, lançado pela Gibson em 1962, foi o primeiro pedal fuzz comercialmente disponível. Embora as vendas iniciais fossem lentas, o destino do pedal mudou drasticamente após Keith Richards dos Rolling Stones utilizá-lo de forma proeminente na faixa "(I Can't Get No) Satisfaction" em 1965. O riff icônico da música, gravado com o Fuzz-Tone, impulsionou o pedal para o mainstream, gerando um enorme aumento no interesse e na demanda pelo efeito fuzz em todo o mundo. Este evento demonstrou de forma contundente como a validação artística pode transformar uma inovação técnica em um fenômeno cultural

### Princípios Eletrônicos do Efeito Fuzz

Para compreender o funcionamento de um pedal fuzz, é fundamental distinguir o efeito de outras formas de saturação e distorção sonora. No cerne, qualquer distorção sônica é o resultado de uma onda sonora sendo impulsionada além da capacidade do dispositivo pelo qual ela passa, seja uma válvula de amplificador ou um circuito eletrônico. Isso causa o "corte" ou "achatamento" (clipping) da onda em seus picos e vales, alterando a qualidade do som resultante.   

-Overdrive: Caracteriza-se por um "rosnado" quente e suave, resultante de um clipping mais brando. Este efeito simula a saturação natural de um amplificador valvulado quando é "empurrado" até o limite de sua capacidade, produzindo uma distorção orgânica e responsiva ao toque do guitarrista.   

-Distorção: Envolve um clipping mais intenso que o overdrive, mas geralmente mais controlado e com maior ganho. Pedais de distorção tendem a produzir um som mais comprimido e sustentado do que os de overdrive, com uma saturação mais uniforme em todo o sinal.   

-Fuzz: Representa a forma mais extrema de distorção, onde as ondas sonoras são "clipadas" com a maior intensidade. Isso achata drasticamente os picos e vales da onda, aproximando-a de uma forma de onda quadrada. O resultado é um som "confuso", "peludo" ou "serrado", com uma aspereza e granulosidade distintas, que o diferencia claramente do overdrive e da distorção mais suave. A principal distinção é a severidade do clipping, que no fuzz é o mais agressivo.   

### Mecanismos de Saturação e Clipping

O funcionamento do fuzz baseia-se fundamentalmente no aumento do ganho do sinal da guitarra e na introdução intencional de distorção harmônica. O "quadramento" dos picos do sinal original é o princípio fundamental do efeito fuzz, transformando a onda senoidal suave de uma guitarra em algo mais próximo de uma onda quadrada.   

Existem dois tipos principais de clipping que influenciam o caráter tonal do fuzz:

-Clipping Simétrico: Este método distorce o sinal de forma uniforme tanto nos lados positivos quanto nos negativos da forma de onda. O resultado é um fuzz mais suave e equilibrado, com um caráter mais musical e menos agressivo. O Electro-Harmonix Big Muff Pi, introduzido em 1969, é um exemplo clássico de pedal que utiliza clipping simétrico para produzir um "fuzz aveludado".   

-Clipping Assimétrico: Neste método, o sinal é distorcido de forma desigual nos semiciclos positivo e negativo, resultando em um som mais áspero e agressivo. O Fuzz Face, por exemplo, exibe um clipping assimétrico que pode variar de suave a "hard clipping" dependendo da ação do potenciômetro de fuzz, contribuindo para sua resposta dinâmica ao volume da guitarra.   

### Geração e Impacto do Conteúdo Harmônico e Sustain

A distorção harmônica é um elemento crucial na sonoridade do fuzz. Ela ocorre quando harmônicos, que são múltiplos da frequência fundamental da nota original, são adicionados ao sinal de áudio. O fuzz, em particular, introduz os harmônicos de ordem mais alta e mais fortes, o que pode ser percebido como um som mais "áspero" ou "estridente".   

A natureza desses harmônicos tem um impacto significativo no timbre percebido:

-Harmônicos de Ordem Par: Múltiplos pares da frequência fundamental (e.g., 2x, 4x) são geralmente mais agradáveis ao ouvido humano e são associados a um som "quente", "encorpado" e "musical". Equipamentos valvulados são conhecidos por gerar uma quantidade significativa de harmônicos pares.   

-Harmônicos de Ordem Ímpar: Múltiplos ímpares da frequência fundamental (e.g., 3x, 5x, 7x) tendem a ser menos agradáveis e contribuem para uma forma de onda mais quadrada e um som mais "duro" ou "áspero". O fuzz, ao "quadrar" o sinal, gera uma grande quantidade de harmônicos ímpares, o que contribui para sua característica "serrada" e agressiva.   

Além da riqueza harmônica, o efeito fuzz aumenta significativamente o sustain do sinal da guitarra, permitindo que as notas soem por um período de tempo prolongado. O Big Muff é particularmente famoso por seu "sustain cremoso, semelhante a um violino", uma característica altamente valorizada por guitarristas que buscam notas longas e expressivas.   

### Topologia do Pedal Fuzz Face

O Fuzz Face, lançado em 1966 pela Dallas Arbiter, é notável por sua simplicidade e eficácia, tornando-se um ícone instantâneo. Seu circuito típico utiliza apenas onze componentes: dois transistores (inicialmente de germânio, depois de silício), quatro resistores, três capacitores e dois potenciômetros. O ganho do circuito é determinado pela relação de valores entre os resistores, permitindo um controle sobre a intensidade do efeito.  

Originalmente, o Fuzz Face utilizava transistores de germânio, como os Mullard OC75s ou NKT275s, que eram valorizados por seu timbre orgânico e responsivo. Posteriormente, foram substituídos por transistores de silício para maior estabilidade e consistência na produção em massa. A seleção cuidadosa dos transistores de germânio é crucial para o desempenho ideal, com a recomendação de um transistor de baixo ganho (β≈70-80) no primeiro estágio e um de alto ganho (β≈110-130) no segundo estágio para alcançar o timbre desejado.
A impedância de entrada do Fuzz Face é relativamente baixa, variando aproximadamente entre 5kΩ e 8.4kΩ. Essa característica faz com que ele "carregue" os captadores da guitarra, o que significa que ele absorve parte da energia do captador e amortece seu pico de ressonância, influenciando diretamente o timbre e a interação com os controles de volume e tom da guitarra. Essa baixa impedância é a razão pela qual é crucial que o Fuzz Face seja o primeiro pedal na cadeia de sinal, logo após a guitarra, pois ele não responde bem se precedido por pedais com buffer, que alteram a impedância do sinal.   


<p align="center">
  Imagem 2: Pedal Fuzz Face
</p>
<p align="center">
<img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/2230516e-248f-466f-8942-7b1109c344c4" />
</p>
<p align="center">
  Fonte: Google Imagens
</p>

### Componentes Eletrônicos e Seu Papel no Circuito Fuzz

### Transistores

Os transistores são os componentes ativos fundamentais em pedais fuzz, atuando como os "amplificadores" do sinal. Eles recebem o sinal da guitarra, o amplificam e, simultaneamente, introduzem a distorção característica do fuzz. O grau e o tipo de distorção são intrinsecamente ligados ao tipo de transistor utilizado e à sua configuração no circuito.   

A escolha entre transistores de germânio e silício é uma das decisões mais impactantes no design de um pedal fuzz, determinando grande parte de seu caráter tonal e comportamento:

-**Transistores de Germânio**: Representam uma tecnologia mais antiga, predominante nos primeiros pedais fuzz dos anos 1950 e 1960. Possuem um ganho inferior (hFe típico entre 70 e 120) em comparação com os de silício. São notavelmente mais sensíveis a variações de temperatura e tensão, o que pode torná-los imprevisíveis em diferentes ambientes, mas também confere-lhes um caráter mais dinâmico e expressivo. Produzem uma distorção descrita como mais "quente, suave e orgânica" , com uma resposta de frequência mais limitada, resultando em um som mais vintage ou retrô. Uma característica muito valorizada é a capacidade de "limpar" o som de forma transparente e orgânica ao reduzir o volume da guitarra. A definição da nota tende a permanecer mais clara mesmo com distorção intensa, e o ataque é menos imediato, conferindo uma sensação de "esponjosidade" ou "saltitante".   

-**Transistores de Silício**: São mais comumente utilizados em pedais fuzz modernos. Oferecem alto ganho (podendo atingir hFe de 400 ou mais)  e uma distorção mais "apertada" e controlada, com uma resposta de frequência mais ampla, o que significa que podem produzir uma gama mais estendida de tons. Têm uma condutividade mais eficiente e consistente, resultando em um som com mais presença de agudos que ajuda a "cortar" na mixagem. Ao contrário do germânio, o silício oferece menos "esponjosidade" e tende a entregar uma "parede de som" mais consistente, ideal para riffs de power chords e leads que precisam se destacar. O "clean up" com o volume da guitarra é mais transparente e claro.

A escolha entre transistores de germânio e silício é fundamental e define o caráter central do pedal. O germânio oferece timbres vintage, dinâmicos e sensíveis ao toque, mas com a desvantagem da sensibilidade à temperatura. O silício, por sua vez, proporciona consistência, maior ganho e, muitas vezes, um som moderno mais agressivo. Essa escolha influencia diretamente a percepção do "sentimento" e da "resposta" do pedal.

### Diodos

Os diodos são componentes semicondutores utilizados para "clipar" o sinal, o que significa cortar as partes superior e inferior da forma de onda, criando a borda nítida e "quadrada" característica do fuzz e da distorção. Ao contrário dos resistores, os diodos são unidirecionais, permitindo que a corrente flua em apenas uma direção.   

Existem diferentes tipos de clipping que podem ser alcançados com diodos:

-**Hard Clipping**: Configurações de diodos onde eles são ligados diretamente ao terra, criando um ponto de corte "duro" e abrupto na forma de onda. Isso resulta em um som agressivo e "quadrado", típico de muitos pedais de distorção.   

-**Soft Clipping**: Diodos inseridos em um caminho de feedback, geralmente em circuitos baseados em amplificadores operacionais. Essa configuração suaviza as bordas do sinal clipado, levando a um tom mais suave e "semelhante a um amplificador valvulado", frequentemente encontrado em overdrives.   

A simetria do clipping também é uma consideração importante:

-**Clipping Simétrico**: Ocorre quando o mesmo número de diodos é usado em cada lado do sinal, resultando em um corte uniforme. Isso tende a produzir um som mais suave e uniforme.   

-**Clipping Assimétrico**: Envolve um número desigual de diodos ou o uso de diferentes tipos de diodos em cada lado. Isso pode resultar em um som percebido como mais alto, claro e "crocante".   

Diferentes tipos de diodos têm diferentes tensões de condução (Forward Voltage - FV), o que determina a quantidade de clipping que ocorre:

-**Diodos de Germânio**: Possuem um FV mais baixo (aproximadamente 0.3V), resultando em um clipping mais pesado, maior compressão e um som mais orgânico.   

-**Diodos de Silício**: Têm um FV moderado (aproximadamente 0.7V) e são comuns em pedais modernos, oferecendo uma distorção moderada sem excesso de compressão.   

### Capacitores

Os capacitores são componentes passivos essenciais em circuitos de pedais de guitarra, com a capacidade de armazenar e liberar energia elétrica. Eles desempenham várias funções cruciais:   

-**Filtragem**: São amplamente utilizados para filtrar frequências indesejadas do sinal, como ruídos de alta frequência (hiss) ou de baixa frequência (rumble). Isso contribui para refinar o timbre da guitarra e garantir um som mais limpo.   

-**Acoplamento**: Capacitores são empregados entre diferentes estágios de um circuito para transferir o sinal de áudio (AC) de um estágio para o próximo, enquanto bloqueiam a corrente contínua (DC) presente no bias de cada estágio. Isso isola os pontos de polarização e permite que cada seção do circuito opere de forma independente.   

-**Controle de Tom**: Em circuitos de controle de tom, os capacitores trabalham em conjunto com resistores para moldar a resposta de frequência do pedal. Ao selecionar valores específicos de capacitância, os designers podem enfatizar ou atenuar certas faixas de frequência, esculpindo o caráter tonal geral do pedal. Por exemplo, um capacitor de maior valor em um circuito de tom pode resultar em um som mais quente e com mais graves, enquanto um de menor valor pode produzir um timbre mais brilhante e focado nos agudos.   

-**Suavização (Smoothing)**: Em fontes de alimentação, capacitores de grande valor são usados para suavizar as ondulações e o ruído na tensão DC, garantindo uma alimentação mais estável para o circuito. Capacitores menores também são usados para desviar ruídos de alta frequência para o terra.   

-**Timing**: Em efeitos baseados em tempo, como delays ou osciladores de baixa frequência (LFOs), os capacitores são utilizados para definir o tempo de atraso ou a frequência de oscilação, manipulando a dimensão temporal do som.

Os tipos de capacitores mais comuns em pedais de guitarra e seu impacto no som incluem:

-**Capacitores Eletrolíticos**: Geralmente usados para valores de capacitância maiores (1μF e acima). São polarizados e comumente empregados em filtragem de fonte de alimentação e desacoplamento.   

-**Capacitores Cerâmicos**: Usados para valores menores (10pF a 999pF). Não são polarizados e são mais baratos, mas capacitores de filme são geralmente preferidos para aplicações de áudio devido ao seu desempenho sonoro percebido.

### Resistores

Os resistores desempenham um papel fundamental no design de circuitos analógicos para pedais de guitarra, mesmo sendo componentes passivos. Eles são responsáveis por:   

-**Relações de Tensão**: Utilizados para dividir a tensão, criando níveis de voltagem específicos necessários para diferentes partes do circuito. Isso garante que cada componente receba a tensão de operação correta.   

-**Limitação de Corrente**: Restringem o fluxo de corrente para proteger componentes de danos e para controlar a quantidade de corrente que passa por uma parte específica do circuito.   

-**Polarização (Bias)**: Em circuitos baseados em transistores, os resistores são cruciais para definir o ponto de polarização, que determina as características de operação do transistor e, consequentemente, o ganho e o perfil de distorção do pedal.   

-**Modelagem Tonal**: Embora seu impacto direto no timbre seja frequentemente sutil, os resistores podem influenciar o som ao interagir com capacitores para formar redes de filtro que moldam a resposta de frequência. Em alguns circuitos fuzz vintage, sua leve não linearidade pode contribuir para uma saturação harmônica característica.   

Os tipos de resistores mais comuns e suas aplicações incluem:

-**Resistores de Composição de Carbono**: Eram comuns em circuitos de áudio e guitarra vintage. São conhecidos por seu alto ruído térmico, ampla tolerância (±10% a ±20%) e baixa estabilidade a longo prazo. No entanto, em alguns circuitos fuzz vintage, sua leve não linearidade e comportamento dependente da tensão podem adicionar uma saturação harmônica característica. Atualmente, são significativamente mais caros devido à sua raridade.   

-**Resistores de Filme Metálico**: Oferecem excelente precisão (tipicamente ±1%), ruído muito baixo e alta estabilidade térmica. São preferidos em caminhos de sinal limpos, estágios de EQ e aplicações de baixo ruído. Alguns construtores os evitam em circuitos fuzz de estilo vintage devido à percepção de falta de "coloração".   


## Materiais e Métodos

### Materiais
| item | quantidade |
|---|---|
| Protoboard | 1|
| Bateria 9V | 1 |
| Jumpers | x |
| Jack IN STEREO | 1 |
| Jack OUT MONO | 1 |
| Switch DPDT | 1 |
| POT Linear 1k Ohm | 1 |
| POT LOG 500k Ohm | 1 |
| Capacitor 2,2uF Eletrolítico | 1 |
| Capacitor 22uF Eletrolítico | 1 |
| Resistor 330 Ohm | 1 |
| Resistor 33k Ohm | 1 |
| Resistor 100k Ohm | 1 |
| Resistor 8,2k Ohm | 1 |
| Transistor BC109C | 1 |
| Case PVC | 1 |

### Métodos
1. Pesquisa e Referencial Teórico
   - Levantamento de informações sobre circuitos analógicos clássicos utilizados em pedais de efeito, como overdrive, distorção, delay, chorus e reverb;
   - Estudo de princípios eletrônicos aplicados ao processamento de áudio, como amplificação, filtragem e modulação de sinal;
   - Análise de projetos existentes e identificação de possíveis melhorias para otimização do desempenho e redução de ruídos.

2. Projeto e Desenvolvimento dos Circuitos
  - Seleção dos efeitos a serem implementados e escolha dos componentes eletrônicos adequados para cada circuito;
  - Desenvolvimento dos esquemáticos dos circuitos utilizando software de simulação (ex.: LTSpice, Proteus ou KiCad) para validar o funcionamento antes da montagem física.

3. Montagem e Testes dos Circuitos
   - Aquisição dos componentes eletrônicos;
   - Soldagem e montagem dos circuitos em protoboard para testes preliminares;
   - Ajustes e calibração dos circuitos para otimizar o desempenho do efeito.

4. Integração do Efeito e Construção do Protótipo
   - Desenvolvimento do design do gabinete, considerando ergonomia, disposição dos controles e conectores;
   - Construção do gabinete com materiais adequados para garantir durabilidade e proteção dos circuitos eletrônicos.

5. Testes Finais e Validação
   - Avaliação do desempenho geral do pedal, incluindo qualidade sonora, usabilidade e robustez da construção;
   - Ajustes finais conforme necessário para melhorar a experiência do usuário.

6. Documentação e Conclusão
   - Registro detalhado do processo de desenvolvimento, incluindo esquemas elétricos, metodologia de montagem e testes;
   - Análise dos resultados obtidos e identificação de possíveis melhorias futuras;
   - Redação do relatório final do projeto, apresentando os desafios enfrentados, soluções adotadas e conclusões sobre a viabilidade do sistema desenvolvido.
     
## Resultados

Após a compra dos materiais, iniciou-se o processo de montagem, usando os esquemáticos abaixo como guia para desenvolvimento dos componentes na protoboard:
<p align="center">
  Imagem 3: Esquemático Pedal Fuzz Face Clone
</p>
<p align="center">
  <img width="700" height="700" alt="image" src="https://github.com/user-attachments/assets/d103c9cd-a989-4793-a35e-dc961216dc40" />
</p>
<p align="center">
  Fonte: Barbarach BC
</p>

<p align="center">
  Imagem 4: Simulação do Pedal Montado em Protoboard
</p>
<p align="center">
 <img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/64ccc7d0-8147-4311-b9ee-9edbdff9efc9" />
</p>
<p align="center">
  Fonte: Barbarach BC
</p>

A ideia era que o circuito ficasse o mais compacto possível. A montagem final pode ser vista na imagem abaixo:


<p align="center">
  Imagem 5: Montagem Final do Pedal Fuzz
</p>
<p align="center">
 <img width="800" height="500" alt="image" src="https://github.com/user-attachments/assets/153c81d9-8225-4f3b-a1fe-224cd9f4e6c7" />
</p>
<p align="center">
  Fonte: Autor
</p>


Além do pedal em si, foi implementaod um botão DPDT que serve como bypass: em um estágio, o sinal vindo da guitarra passa pelo circuito e é alterado pelo mesmo. Já no outro estágio do botão, o sinal limpo da guitarra passa direto para o amplificador, sem passar pelo circuito.

Para proteção do circuito, foi comprada uma case de PVC, que foi furada para que os jacks P10 de entrada e saída, o botão e os dois potenciômetros ficassem com fácil acesso, permitindo usabilidade do pedal.

## Conclusão

### Dificuldades encontradas

A ideia inicial seria executar um circuito com maior grau de complexidade, a escolha era o pedal de efeito Flanger. Porém na hora da compra dos componentes, havia um CI específico que não era mais fabricado, e as poucas unidades restantes no mercados custavam muito caro, inviabilizando o projeto. Também foi estudada a possibilidade de realizar outro tipo de pedal flanger ou outro efeito, já que existem diversos pedais com vários tipos de efeitos diferentes, entretanto, a maioria dos pedais de efeito têm um circuito muito extenso por trás, fazendo com que a montagem em protoboard ou em placa de circuito impressa fique muito complexa e difícil de resolver problemas no circuito, caso algum viesse a aparecer durante a montagem.

### Sugestões para trabalhos futuros

Como melhorias para esse pedal, é recomendado que seja feita a troca da case de PVC por uma case metálica. A case metálica evita que o circuito fique suscetível a interferências eletromagnéticas radiadas pelo ar, podendo causar mal funcionamento ou mudança do sinal de saída esperado.
Ademais, é recomendado que o circuito seja montado em placa de circuito impresso, com as conexões entre os componentes sendo feitas através de solda. Atualmente, com a placa montade em protoboard, pode haver mal contato e até mesmo que os componentes se desconectem da protoboard quando o pedal está sendo movimentado.
Finalmente, é recomendado que seja feita a troca da alimentação do pedal. Hoje ele está sendo alimentado através de uma bateria 9V interna, que por si só funciona perfeitamente, porém, para evitar que seja necessário abrir o pedal para trocar a bateria quando ela descarregar, a substituição para um conector P4 (figura abaixo), assim, seria necessário que o pedal fosse conectado a uma fonte 9V externa, evitando a necessidade da troca de bateria interna.


<p align="center">
  Imagem 6: Jack P4 Fêmea
</p>
<p align="center">
<img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/5f130cb9-4a12-4034-a5f2-8db7cee9d8c6" />
</p>
<p align="center">
  Fonte: Google Imagens
</p>

## Referências
- AIRGIGS. History & evolution of the fuzz pedal (Fuzz Face, Tone Bender & Big Muff). [S. l.], 23 abr. 2019. Disponível em: https://blog.airgigs.com/2019/04/history-evolution-of-the-fuzz-pedal-fuzz-face-tone-bender-big-muff/.
- BOOST GUITAR PEDALS. What are clipping diodes?. [S. l.], 23 nov. 2022. Disponível em: https://www.boostguitarpedals.co.uk/blogs/pedal-knowledge/what-are-clipping-diodes-guitar-pedal.
- CODA EFFECTS. The different types of fuzz. [S. l.], 13 ago. 2015. Disponível em: https://www.coda-effects.com/2015/08/the-different-types-of-fuzz.html?m=0.
- ELECTROSMMASH. Fuzz Face analysis. [S. l.], [20--?]. Disponível em: https://www.electrosmash.com/fuzz-face.
- ELECTROSMMASH. Big Muff Pi analysis. [S. l.], [20--?]. Disponível em: https://www.electrosmash.com/big-muff-pi-analysis.
- GUITAR CENTER. History of the fuzz pedal. [S. l.], 21 jul. 2023. Disponível em: https://www.guitarcenter.com/riffs/gear-tips/amplifiers--effects/history-fuzz-pedal.
- PEDAL PLAYERS. Silicon vs Germanium Fuzz. [S. l.], [20--?]. Disponível em: https://pedalplayers.com/silicon-vs-germanium-fuzz/.
- PEDAL PAWN. Silicon vs Germanium transistors (fuzz pedals explained). [S. l.], 10 fev. 2023. Disponível em: https://pedalpawn.com/it/blogs/news/silicon-vs-germanium-transistors-fuzz-pedals-explained.
- REDDIT. Understanding the fuzz pedal, their components and the values of the components. [S. l.], 2 maio 2024. Disponível em: https://www.reddit.com/r/diypedals/comments/1e31u6a/understanding_the_fuzz_pedal_their_components_and/.
- SLIGHTLY TECHNICAL ACADEMY. Building better pedals: the real role of components in guitar tone. [S. l.], [20--?]. Disponível em: https://www.slightlytechnicalacademy.com/techpages/building-better-pedals-the-real-role-of-components-in-guitar-tone.
- "Building a Fuzz Face Clone - Breadboarding - Barbarach BC". Barbarach BC, 1 de setembro de 2021. Disponível em: https://barbarach.com/building-a-fuzz-face-clone-breadboarding/
- "Building a Fuzz Face Clone – Assembly - Barbarach BC". Barbarach BC, 4 de outubro de 2021. Disponível em: https://barbarach.com/building-a-fuzz-face-clone-assembly/

