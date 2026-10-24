# Automação de Conteúdo para Redes Sociais com n8n e Google Gemini API

## Descrição do Projeto
Fluxo de trabalho automatizado (*workflow*) desenvolvido no **n8n** focado na geração ágil de copys e legendas atrativas para divulgação dos produtos do meu ateliê nas redes sociais (Instagram/Facebook). A solução visa reduzir o tempo gasto na criação manual de conteúdo, mantendo um tom moderno, profissional e com forte apelo visual.

---

## Tecnologias e Ferramentas
- **[n8n](https://n8n.io/):** Orquestrador e automação de fluxos locais.
- **[Google Gemini API](https://ai.google.dev/):** Modelo `gemini-3-flash-preview` para geração das variações de copy.
- **GitHub:** Documentação e versionamento do projeto.

---

## Estrutura do Fluxo no n8n
O fluxo foi construído de forma simples e modular em 3 etapas:
1. **Ao clicar em 'Executar fluxo de trabalho' (Manual Trigger):** Ponto de partida manual para disparar a automação sob demanda.
2. **Editar campos (Edit Fields):** Define as propriedades dinâmicas do produto. No teste prático:
   - Campo `produto`: `"sacochila em brim e courino"`
3. **Enviar mensagem para um modelo (Google Gemini):**
   - **Modelo:** `models/gemini-3-flash-preview`
   - **Prompt utilizado:**
     > `"Crie um texto curto e atrativo para publicação nas redes sociais divulgando o seguinte produto: {{ $json.produto }}"`
   - O nó consome a variável do produto e devolve opções segmentadas por estilo, com emojis, chamadas para ação (CTA) e hashtags.

---

## Resultado Gerado
A API retornou opções completas de copy prontas para uso. Exemplo de saída:
> **Opção focada em Estilo (Instagram):**  
> *"O básico que de básico não tem nada! ✨ Procurando o acessório perfeito para te acompanhar do treino ao rolê? Nossa nova sacochila une a resistência do brim com o toque sofisticado do courino. 🔥 Mochila moderna, versátil e com aquele design que combina com qualquer look..."*  
> **Hashtags geradas:** `#mochila #sacochila #estilourbano #acessorios #brimecourino #lookdodia`

---

## Reflexão: "Natty or Not?" (Natural ou Fake?)
- **Veredito:** **Natty (Natural)**.
- **Análise:** O modelo `gemini-3-flash` entregou uma linguagem descontraída, persuasiva e alinhada com as boas práticas de copywriting para redes sociais, sem soar como um texto gerado mecanicamente. A possibilidade de gerar múltiplos tons (estilo, benefícios, casual) traz flexibilidade ao negócio sem perder a identidade artesanal da marca.

---

## Evidências de Execução

### 1. Visão Geral do Workflow Executado
<img width="1117" height="542" alt="Captura de tela 2026-10-23 212804" src="https://github.com/user-attachments/assets/122709d1-1ad9-4525-b2a4-1adfc3cf9570" />
### 2. Parâmetros do Nó Gemini e Resultado Obtido
<img width="1840" height="806" alt="Captura de tela 2026-10-23 205345" src="https://github.com/user-attachments/assets/4daf78b8-f87a-4917-b210-8d5b5c7357fa" />
