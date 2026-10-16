# Stuck On Set — Relatórios de Bugs e Observações de QA

Este documento reúne problemas técnicos aparentes, dificuldades de usabilidade, observações de balanceamento e sugestões de melhoria identificados durante um teste exploratório independente.

## Contexto do Teste

- **Jogo:** Stuck On Set
- **Data do teste:** 16/10/2026
- **Versão:** Version 7, disponível desde 13/10/2026
- **Plataforma:** PC
- **Dispositivo principal:** Teclado e mouse
- **Dispositivo adicional:** Controle/gamepad
- **Abordagem:** Teste exploratório independente, baseado na experiência do jogador, sem roteiro predefinido.
- **Ambiente:** Executável final, sem acesso ao código-fonte ou ao ambiente de desenvolvimento.
- **Origem do projeto:** Prática independente de QA por meio do Play2Review.

### Como interpretar os relatos

Os relatos abaixo descrevem o comportamento observado e seu possível impacto para o jogador. As prioridades são sugestões de classificação para fins de portfólio, não prioridades oficiais atribuídas pelos desenvolvedores.

- **Bug técnico aparente:** comportamento que parece incorreto ou inconsistente.
- **Usabilidade:** comportamento que dificulta compreender ou utilizar o jogo.
- **Balanceamento/design:** percepção subjetiva sobre eficácia, dificuldade ou funcionamento de uma mecânica.
- **Sugestão:** proposta de melhoria que não pressupõe a existência de um defeito.

As causas técnicas não foram confirmadas. Os relatos não foram retestados em versões posteriores.

---

# Problemas Técnicos Aparentes

## BUG-001 — Movimentação inconsistente pelo teclado

**Categoria:** Controles / Movimentação  
**Prioridade sugerida:** Alta  
**Tipo:** Bug técnico aparente

### Descrição

A movimentação horizontal parece significativamente mais rápida do que a movimentação para frente e para trás. Além disso, pressionar duas direções simultaneamente não parece produzir uma movimentação diagonal consistente.

O comportamento aparentemente não se manifesta da mesma forma ao utilizar um controle.

### Impacto

A movimentação inconsistente prejudica a precisão dos deslocamentos e pode tornar os combates e as esquivas mais difíceis.

### Passos de reprodução

1. Iniciar uma partida utilizando teclado e mouse.
2. Movimentar o personagem horizontalmente.
3. Movimentar o personagem para frente e para trás.
4. Comparar as velocidades percebidas.
5. Pressionar duas direções simultaneamente e observar a movimentação diagonal.

**Limitação:** Não foram realizadas medições objetivas de velocidade. A diferença foi observada durante o jogo.

---

## BUG-002 — Menus aparentemente incompatíveis com o controle

**Categoria:** Controles / Interface  
**Prioridade sugerida:** Média  
**Tipo:** Bug técnico aparente

### Descrição

Durante o teste, os menus não pareceram totalmente interativos com o controle/gamepad.

### Impacto

Jogadores que preferem utilizar o controle podem ter dificuldade para navegar pela interface ou acessar determinadas opções.

### Passos de reprodução

A interação inconsistente foi observada durante o uso do controle. Não foram registrados passos detalhados suficientes para especificar quais elementos do menu falharam em cada situação.

---

## BUG-003 — Dash pode ser acionado com no menu principal

**Categoria:** Controles / Interface  
**Prioridade sugerida:** Baixa  
**Tipo:** Comportamento a verificar

### Descrição

Foi possível acionar o dash enquanto estava no menu principal, embora a movimentação normal do personagem não parecesse funcionar.

### Impacto

O comando pode ser ativado acidentalmente durante a navegação pela interface.

### Passos de reprodução

1. Abrir o menu principal do jogo.
2. Pressionar o comando de dash.
3. Observar se o personagem executa a ação.

**Observação:** Não foi possível determinar se esse comportamento é intencional.

---

## BUG-004 — Instruções incorretas para o comando de dash

**Categoria:** Tutorial / Controles  
**Prioridade sugerida:** Média  
**Tipo:** Inconsistência de documentação

### Descrição

O tutorial indica RT/R2 para executar o dash. Durante o teste, RT/R2 disparava a arma, enquanto RB/R1 executava o dash.

### Impacto

As instruções podem levar o jogador a utilizar o comando incorreto, especialmente durante os primeiros minutos de jogo.

### Resultado esperado

As instruções exibidas no tutorial devem corresponder aos comandos efetivamente configurados.

---

## BUG-005 — Colisões incorretas com paredes

**Categoria:** Física / Colisão  
**Prioridade sugerida:** Média  
**Tipo:** Bug técnico aparente

### Descrição

Algumas colisões com paredes pareceram inconsistentes com a geometria visível do cenário.

### Impacto

O comportamento pode prejudicar a movimentação e gerar a impressão de que o personagem está colidindo com obstáculos invisíveis ou atravessando limites inadequados.

### Evidência

O comportamento foi observado durante o teste. A existência de uma gravação de apoio não implica que ela esteja publicada neste repositório.

**Limitação:** Não foram documentados passos de reprodução suficientemente precisos para estabelecer um cenário específico.

---

## BUG-006 — Inimigos surgem parcialmente dentro do chão

**Categoria:** Spawn / Física  
**Prioridade sugerida:** Média  
**Tipo:** Bug técnico aparente

### Descrição

Alguns inimigos pareceram surgir parcialmente dentro do chão e, em determinadas situações, ficaram incapazes de se movimentar. Ainda assim, aparentemente podiam ser atingidos por disparos.

### Impacto

O comportamento pode comprometer a movimentação dos inimigos e tornar os encontros de combate inconsistentes.

### Limitação

Não foi possível determinar a causa técnica nem confirmar se o problema ocorre em condições específicas de spawn ou tipo de inimigo.

---

# Usabilidade e Clareza

## OBS-001 — Excesso de elementos visuais na Call Sheet

**Categoria:** Interface / UX  
**Prioridade sugerida:** Baixa  
**Tipo:** Observação de usabilidade

### Descrição

A Call Sheet apresenta muitos elementos visuais e decorativos, tornando menos evidente a separação entre as informações funcionais e os elementos temáticos.

### Impacto

O jogador pode precisar de mais tempo para localizar informações relevantes.

### Sugestão

Separar visualmente as informações funcionais dos elementos decorativos, preservando a identidade visual de produção cinematográfica.

---

## OBS-002 — Tutorial depende excessivamente do manual

**Categoria:** Tutorial / UX  
**Prioridade sugerida:** Média  
**Tipo:** Observação de usabilidade

### Descrição

O tutorial parece pressupor que o jogador consultará o manual para compreender determinados sistemas.

### Impacto

Jogadores que esperam aprender as mecânicas diretamente durante o jogo podem não compreender os controles, as melhorias ou as regras de combate com facilidade.

### Sugestão

Adicionar explicações contextuais curtas para as mecânicas essenciais e permitir que o manual complemente essas informações.

---

## OBS-003 — Contraste insuficiente no menu aberto com ESC

**Categoria:** Interface / Acessibilidade  
**Prioridade sugerida:** Baixa  
**Tipo:** Observação de usabilidade

### Descrição

O menu aberto com ESC utiliza texto branco sobre fundo cinza, o que parece reduzir a legibilidade.

### Sugestão

Aumentar o contraste entre texto e fundo, verificando a legibilidade em diferentes condições de iluminação e configurações de tela.

---

## OBS-004 — Câmera pode ser confundida com um inimigo

**Categoria:** Câmera / Apresentação visual  
**Prioridade sugerida:** Baixa  
**Tipo:** Observação de usabilidade

### Descrição

Em algumas situações, a câmera parece se aproximar excessivamente do cenário ou atravessar elementos da ambientação. Sua aparência chegou a ser confundida com a de um inimigo durante o combate.

### Impacto

O jogador pode interpretar incorretamente elementos do cenário como ameaças e desperdiçar disparos.

### Sugestão

Revisar o comportamento da câmera próximo a objetos e paredes, além de avaliar a clareza visual dos elementos apresentados na tela.

---

## OBS-005 — Diferenças entre inimigos pouco evidentes

**Categoria:** Combate / Clareza visual  
**Prioridade sugerida:** Média  
**Tipo:** Observação de usabilidade

### Descrição

Alguns tipos de inimigos são difíceis de distinguir durante os combates. Foi possível identificar diferenças mais evidentes em certos casos, como o palhaço que utiliza ataques à distância mais lentos e inimigos maiores com mais vida. Outros tipos pareceram semelhantes em comportamento ou ameaça.

### Impacto

A identificação rápida de ameaças e a escolha de prioridades durante o combate podem ser prejudicadas.

### Sugestão

Reforçar diferenças visuais, animações, silhuetas ou padrões de ataque entre os tipos de inimigos.

---

## OBS-006 — Ataques pouco sinalizados e origem do dano pouco clara

**Categoria:** Combate / Feedback ao jogador  
**Prioridade sugerida:** Alta  
**Tipo:** Observação de usabilidade

### Descrição

Alguns ataques não parecem apresentar sinais visuais suficientemente claros antes de causar dano. Além disso, certos comportamentos de projéteis e inimigos parecem inconsistentes, dificultando a identificação da origem do dano recebido.

### Impacto

O jogador pode sentir que recebeu dano de maneira inesperada. Isso também pode dificultar desafios que exigem evitar todo o dano.

### Sugestão

Revisar os sinais visuais e sonoros que antecedem os ataques e tornar mais consistente a relação entre os comportamentos dos inimigos e o dano causado.

---

## OBS-007 — Texto de imunidade do chefe gera dúvidas

**Categoria:** Combate / Clareza de mecânicas  
**Prioridade sugerida:** Média  
**Tipo:** Observação de usabilidade

### Descrição

O texto grande “IMMUNE” exibido durante o encontro com o chefe inicialmente gerou dúvidas sobre como avançar no combate. Não ficou imediatamente claro se era necessário esperar a imunidade terminar, enfraquecer o chefe ou atacar sua proteção.

Posteriormente, foi tentado atacar o escudo do chefe.

### Impacto

O jogador pode não compreender qual ação é necessária para progredir no combate.

### Sugestão

Avaliar se o texto de imunidade e a representação visual do escudo transmitem informações redundantes ou insuficientes. Um indicador contextual pode esclarecer o objetivo sem remover o desafio.

---

## OBS-008 — Ataques do chefe parecem fáceis de esquivar

**Categoria:** Combate / Balanceamento  
**Prioridade sugerida:** Baixa  
**Tipo:** Observação subjetiva de design

### Descrição

Durante o encontro testado, alguns ataques do chefe pareceram relativamente fáceis de evitar com pequenos deslocamentos.

### Impacto

Dependendo da intenção de design, isso pode reduzir o desafio do encontro.

### Limitação

Esta é uma impressão subjetiva baseada na experiência observada. Não foi possível avaliar o balanceamento de chefes posteriores nem determinar a dificuldade pretendida para o encontro.

---

## OBS-009 — Balões do palhaço causam dano quando atingidos

**Categoria:** Combate / Clareza de interação  
**Prioridade sugerida:** Média  
**Tipo:** Comportamento a esclarecer

### Descrição

Os balões do palhaço causam dano ao jogador quando tocados. Durante o teste, disparar contra os balões também pareceu causar dano ao jogador.

Embora o dano por contato pareça compreensível, a consequência de atirar nos balões não ficou clara.

### Impacto

Durante encontros com vários inimigos e projéteis, pode ser difícil evitar os balões e compreender qual ação provocou o dano.

### Sugestão

Se o dano causado ao disparar nos balões for intencional, comunicar essa interação por meio de sinais visuais, sonoros ou instruções contextuais.

---

## OBS-010 — Sentinel Spheres exigem proximidade arriscada

**Categoria:** Combate / Balanceamento  
**Prioridade sugerida:** Baixa  
**Tipo:** Observação subjetiva de design

### Descrição

As Sentinel Spheres orbitam o jogador a uma distância que parece exigir aproximação excessiva dos inimigos para causar dano.

### Impacto

A mecânica pode incentivar o jogador a se expor a ataques para utilizar a melhoria de forma eficaz.

### Sugestão

Avaliar a distância de órbita e a relação entre risco, alcance e eficácia da melhoria.

---

## OBS-011 — Melhoria de duas armadilhas pequenas parece menos controlável

**Categoria:** Melhorias / Balanceamento  
**Prioridade sugerida:** Baixa  
**Tipo:** Observação subjetiva de design

### Descrição

A melhoria que produz duas armadilhas pequenas pareceu menos previsível ou menos eficaz, na prática, do que utilizar uma única armadilha.

### Impacto

O jogador pode perceber a melhoria como pouco vantajosa ou difícil de utilizar de forma consistente.

### Sugestão

Revisar a distribuição, a área de efeito e a eficácia das armadilhas para que a melhoria apresente vantagens compreensíveis.

---

## OBS-012 — Precisão limitada da Ol' Painless a longa distância

**Categoria:** Armas / Balanceamento  
**Prioridade sugerida:** Baixa  
**Tipo:** Observação subjetiva de design

### Descrição

A Ol' Painless apresenta uma cadência de tiro razoável, e a restrição de movimentação durante os disparos pareceu menos problemática do que o esperado. Entretanto, sua precisão a longa distância parece limitada, com poucos projéteis atingindo os alvos.

Não foi identificada uma forma evidente de melhorar a precisão por meio da mira ou das melhorias disponíveis durante o teste.

### Impacto

A arma pode parecer pouco confiável em combates a distância.

### Sugestão

Avaliar a precisão, a dispersão e as opções disponíveis para melhorar a eficácia da arma em diferentes alcances.

---

## OBS-013 — Galleria Shotgun pode estar forte demais

**Categoria:** Armas / Balanceamento  
**Prioridade sugerida:** Baixa  
**Tipo:** Observação subjetiva de design

### Descrição

A Galleria Shotgun proporcionou uma experiência satisfatória e pareceu ser uma das opções mais eficazes entre as armas testadas.

### Impacto

Caso a diferença de eficácia em relação às outras armas seja excessiva, isso pode reduzir o incentivo à experimentação.

### Limitação

Não foram realizadas medições de dano ou testes comparativos controlados. A observação reflete a experiência durante a sessão.

---

## OBS-014 — Relação entre Genre, melhorias e vida máxima pouco clara

**Categoria:** Progressão / UX  
**Prioridade sugerida:** Média  
**Tipo:** Observação de usabilidade

### Descrição

A aquisição e a utilização dos pontos de Genre não ficaram suficientemente claras. Melhorias consideradas relevantes parecem exigir o sacrifício de vida máxima.

### Impacto

O jogador pode ter dificuldade para compreender os custos, benefícios e consequências das decisões de progressão.

### Sugestão

Explicar com maior clareza a aquisição dos pontos, os custos das melhorias e as consequências de sacrificar vida máxima.

---

## OBS-015 — Tempo de preparação das armadilhas pouco evidente

**Categoria:** Combate / Feedback ao jogador  
**Prioridade sugerida:** Baixa  
**Tipo:** Observação de usabilidade

### Descrição

Em algumas situações, os inimigos passaram sobre armadilhas posicionadas pelo jogador sem que parecesse ocorrer qualquer efeito. Posteriormente, ficou mais claro que as armadilhas possuem um período de preparação.

O comportamento parece fazer parte da mecânica, mas o tempo necessário para a ativação não ficou evidente inicialmente.

### Impacto

O jogador pode interpretar a ausência de efeito como uma falha da armadilha.

### Sugestão

Comunicar o estado de preparação por meio de animação, indicador visual ou efeito sonoro.

---

## OBS-016 — Orçamento parece permitir comprar a maioria das melhorias

**Categoria:** Economia / Balanceamento  
**Prioridade sugerida:** Baixa  
**Tipo:** Observação subjetiva de design

### Descrição

O orçamento disponível parece generoso, permitindo adquirir boa parte das melhorias apresentadas.

### Impacto

Se a intenção for incentivar decisões difíceis de alocação de recursos, a economia pode não criar escolhas suficientemente relevantes.

### Limitação

Não foi possível determinar se o orçamento generoso é intencional, especialmente considerando a possibilidade de a versão testada servir também para avaliar sistemas em desenvolvimento.

---

## OBS-017 — Oferecer várias opções para a próxima rodada

**Categoria:** Sugestão de design  
**Prioridade sugerida:** Informativa  
**Tipo:** Sugestão de melhoria

### Descrição

Uma possibilidade seria oferecer mais de uma opção de próxima rodada ou encontro, de maneira semelhante à seleção de caminhos e encontros presente em jogos como *Hades*.

### Benefício potencial

Isso poderia aumentar a variedade das partidas e permitir que o jogador influenciasse o tipo de desafio ou recompensa que deseja buscar.

### Limitação

Esta é uma sugestão de design, não um relato de defeito.

---

# Limitações do Teste

- O teste foi realizado em 16/10/2026, na Version 7, disponível desde 13/10/2026.
- A sessão foi exploratória e baseada na experiência do jogador, sem roteiro predefinido.
- Os passos de reprodução foram incluídos somente quando o comportamento podia ser descrito claramente usando o executável final.
- As causas técnicas dos comportamentos não foram estabelecidas.
- Os relatos não foram retestados em versões posteriores.
- Não foram observadas nem relatadas quedas de desempenho, travamentos ou outros problemas de performance durante a sessão.
- Nenhum sistema de meta-progressão foi percebido durante o teste. Sua existência ou ausência não foi verificada de forma independente.

A ausência de um problema relatado não comprova que o sistema correspondente esteja livre de defeitos.

# Feedback e Correções

Estes relatórios foram elaborados de forma independente para prática de QA por meio do Play2Review. As observações representam a experiência do jogador e não foram confirmadas pelos desenvolvedores.

Caso algum relato esteja incorreto, já tenha sido corrigido ou precise de contexto adicional, estou aberto a revisar a documentação.

Os desenvolvedores podem entrar em contato para discutir possíveis correções ou a remoção de materiais específicos. Este repositório poderá ser atualizado com base no feedback recebido sobre as observações enviadas pelo Play2Review.
