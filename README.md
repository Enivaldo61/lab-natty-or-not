# Projeto: Gerador Ágil de Legendas de Produtos com n8n & IA

## Descrição do Projeto
Este projeto foi desenvolvido como parte do Desafio de Projeto "Natty or Not" da Digital Innovation One (DIO). O objetivo principal é construir uma automação simples e didática utilizando a plataforma n8n conectada a um Modelo de Linguagem (IA Generativa), permitindo a geração rápida e estruturada de legendas para divulgação de produtos em redes sociais e canais de atendimento.

O projeto beneficia pequenos empreendedores e criadores de conteúdo que buscam agilidade na comunicação sem perder a clareza e o tom humanizado.

## Tecnologias e Ferramentas Utilizadas
- **n8n:** Orquestração do fluxo de automação e integração de nós.
- **OpenAI / Gemini:** Processamento e geração do conteúdo textual via IA Generativa.
- **GitHub:** Documentação, versionamento e publicação do repositório.

## Arquitetura do Fluxo no n8n
O fluxo foi estruturado em um pipeline simples de 3 etapas principais:

1. **Entrada (Trigger):** Utilização do nó *Manual Trigger* (ou Formulário simples) para receber a descrição do produto e as especificações básicas.
2. **Processamento (Nó de IA):** Chamada ao modelo de IA Generativa via prompt instrucional focado em síntese e engajamento.
3. **Saída (Visualização):** Exibição do resultado gerado diretamente na interface do n8n para validação do usuário.

## Prompts e Exemplos de Entrada/Saída

- **Prompt Utilizado:**
  > `"Aja como um assistente especialista em comunicação e marketing. Crie uma legenda curta, clara e engajadora com emojis para divulgação do seguinte produto: [Entrada do Usuário]. Mantenha um tom profissional e acolhedor."`

- **Exemplo de Entrada:**
  > *"Bandana pet confeccionada em tecido de algodão, tamanho P, estampa xadrez verde."*

- **Exemplo de Saída Gerada:**
  > *"Seu pet com o estilo que ele merece! 🐾 Conheça nossa nova bandana xadrez verde em algodão, leve e confortável para o dia a dia. Garanta já o tamanho P para o seu companheiro!"*

## Reflexão ("Natty or Not")
- **Natty (Natural) ou Fake Natty (Artificial)?** 
  O resultado gerado mostrou-se **Natty (Natural)**. O modelo conseguiu balancear os emojis e a mensagem sem exageros ou clichês robóticos, mantendo a utilidade prática para o dia a dia.
- **Experiência com n8n:**
  Orquestrar a IA através do n8n demonstra o potencial da automação visual: em vez de digitar prompts manualmente a todo momento, o fluxo padroniza a entrada e a saída, economizando tempo e mantendo a consistência do conteúdo.
