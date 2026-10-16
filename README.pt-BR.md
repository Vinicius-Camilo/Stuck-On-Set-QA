# Relatório de teste de jogo - Stuck On Set

Documentação de um teste exploratório independente do jogo *Stuck On Set*, com foco em identificação de possíveis bugs, usabilidade, clareza de combate e experiência do jogador.

## Contexto do Projeto

Este projeto foi desenvolvido de forma independente para praticar QA (Quality Assurance) por meio da plataforma Play2Review.

O objetivo é documentar observações obtidas durante a experiência prática com o jogo, identificar possíveis defeitos e problemas de usabilidade e exercitar a elaboração de relatórios de QA estruturados.

O teste foi realizado no executável do jogo, sem acesso ao código-fonte ou ao ambiente de desenvolvimento.

Este repositório é um projeto independente de portfólio. Não representa um relatório oficial de QA nem possui vínculo formal com os desenvolvedores do jogo.

## Informações do Teste

| Campo | Detalhes |
|---|---|
| Jogo | Stuck On Set |
| Página do jogo | [itch.io — Stuck On Set](https://driftingsignal.itch.io/stuck-on-set) |
| Data do teste | 16/10/2026 |
| Versão testada | Version 7 |
| Disponibilidade da versão | 13/10/2026 |
| Tipo de teste | Exploratório |
| Plataforma de teste | PC |
| Dispositivo principal | Teclado e mouse |
| Dispositivo adicional | Controle/gamepad |
| Ambiente de teste | Executável final disponível ao jogador |
| Ferramenta de gravação | OBS Studio, utilizado durante a sessão, sem gravação publicada neste repositório |

## Abordagem de Teste

O teste foi conduzido de maneira exploratória, com base na minha experiência como jogador de longa data. Não foi utilizado um roteiro de testes predefinido nem uma suíte formal de casos de teste.

Durante a sessão, explorei os controles, menus, armas, melhorias, armadilhas, inimigos, combates e outros sistemas disponíveis na versão testada.

Os relatos refletem comportamentos observados durante a experiência de jogo. Os passos de reprodução foram incluídos somente quando era possível descrever o comportamento com clareza usando o executável disponível, sem acesso ao código-fonte ou ao ambiente de desenvolvimento.

As observações não devem ser interpretadas automaticamente como defeitos confirmados. Alguns comportamentos podem ser escolhas intencionais de design, limitações conhecidas ou problemas que exigem investigação adicional.

## Principais Observações

### Controles e movimentação

- A movimentação pelo teclado parece apresentar diferenças de velocidade entre os eixos horizontal e vertical.
- A movimentação diagonal não parece funcionar de maneira consistente.
- Os menus não parecem ser totalmente utilizáveis com o controle.
- O tutorial apresenta instruções incorretas para o comando de dash.
- O dash é responsivo e fluido, mas a experiência geral de movimentação é prejudicada pelos problemas observados.

### Combate e inimigos

- Algumas diferenças entre os tipos de inimigos são difíceis de identificar durante o combate.
- Certos ataques não parecem apresentar sinais visuais suficientemente claros antes de causar dano.
- Alguns comportamentos de projéteis e inimigos tornam a origem do dano difícil de compreender.
- Alguns inimigos parecem surgir parcialmente dentro do chão e podem ficar incapazes de se movimentar.
- O texto de imunidade do chefe pode gerar dúvidas sobre como superar sua defesa.
- Os balões do palhaço causam dano quando tocados e também quando são atingidos por disparos, comportamento cuja intenção não ficou clara durante o teste.

### Armas, melhorias e progressão

- A Galleria Shotgun proporcionou uma experiência de combate satisfatória, mas pareceu potencialmente mais forte do que as demais opções testadas.
- A Ol' Painless apresenta uma cadência de tiro razoável, mas sua precisão em longas distâncias parece limitada.
- As Sentinel Spheres podem exigir que o jogador se aproxime perigosamente dos inimigos.
- A melhoria que cria duas armadilhas pequenas parece oferecer menos controle do que uma única armadilha.
- A relação entre pontos de Genre, melhorias e sacrifício de vida máxima não ficou suficientemente clara.
- O orçamento disponível parece generoso, permitindo adquirir boa parte das melhorias apresentadas. Não foi possível determinar se isso é intencional.

### Interface e usabilidade

- A Call Sheet apresenta muitos elementos visuais, dificultando a identificação das informações funcionais.
- O tutorial parece depender excessivamente da leitura do manual para explicar alguns sistemas.
- O menu aberto com ESC apresenta texto branco sobre fundo cinza, com contraste aparentemente insuficiente.
- A câmera ocasionalmente parece atravessar ou se aproximar excessivamente do cenário, podendo ser confundida com um inimigo.
- O tempo de preparação das armadilhas não fica suficientemente evidente, embora o comportamento pareça fazer parte da mecânica.

## Aspectos Positivos

- O dash é responsivo e agradável de utilizar.
- A temática de produção cinematográfica oferece uma identidade interessante ao jogo.
- As missões de sobrevivência em ambientes fechados proporcionam combates intensos e envolventes.
- A Galleria Shotgun oferece uma sensação satisfatória de impacto e eficácia.
- O sistema de armas e melhorias incentiva a experimentação.
- O combate tem bons momentos, apesar das dificuldades de clareza observadas.

## Limitações do Teste

- O teste foi realizado em 16/10/2026, utilizando a Version 7, disponível desde 13/10/2026.
- A abordagem foi exploratória e baseada na experiência do jogador, sem roteiro de testes predefinido.
- Os passos de reprodução foram documentados somente quando podiam ser descritos claramente a partir do executável final.
- As causas técnicas dos comportamentos relatados não foram investigadas nem confirmadas.
- Os resultados não foram retestados em versões posteriores.
- Não foram observadas nem relatadas quedas de desempenho, travamentos ou outros problemas de performance durante a sessão.
- Nenhum sistema de meta-progressão entre partidas foi identificado de maneira perceptível. Sua existência ou ausência não foi verificada de forma independente.

A ausência de um problema relatado não significa que o sistema correspondente esteja livre de defeitos.

## Estrutura do Repositório

- `README.md` — apresentação do projeto em inglês.
- `README.pt-BR.md` — apresentação do projeto em português brasileiro.
- `bug-reports.md` — relatórios de bugs e observações em inglês.
- `bug-reports.pt-BR.md` — relatórios de bugs e observações em português brasileiro.

## Feedback e Correções

Feedback dos desenvolvedores é bem-vindo. Caso alguma observação esteja incorreta, já tenha sido corrigida ou precise de contexto adicional, estou aberto a revisar e corrigir a documentação.

Caso existam preocupações sobre o conteúdo deste repositório, os desenvolvedores podem entrar em contato para discutir possíveis correções ou a remoção de materiais específicos.

Este repositório poderá ser atualizado com base no feedback dos desenvolvedores sobre as observações enviadas por meio do Play2Review.

## Conclusão

O teste identificou oportunidades de melhoria relacionadas à consistência dos controles, à clareza dos ataques, à diferenciação dos inimigos, à comunicação das mecânicas e à hierarquia visual da interface.

O jogo também apresentou aspectos positivos, especialmente na responsividade do dash, na identidade temática e na sensação de combate proporcionada por determinadas armas.

Os relatos representam observações de uma única sessão exploratória e devem ser interpretados dentro das limitações descritas neste documento.
