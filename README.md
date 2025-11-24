# Agente tutor para auxiliar nos estudos preparatórios para o exame CCNA da Cisco

Este repositório contém o desenvolvimento de um agente tutor inteligente criado no Microsoft AI Foundry, projetado para auxiliar estudantes nos estudos para a certificação **Cisco CCNA**.  
Ele responde dúvidas teóricas, gera exercícios, explica conceitos de redes, cria exemplos de configuração Cisco IOS e sugere trilhas de estudo.

---

## Descrição do Agente

- Explicar conceitos essenciais e rede (OSI, TCP/IP, VLANs, STP, IP addressing, etc...)
- Fornecer exemplos reais de configurações Cisco.  
- Criar quizzes personalizados conforme o tema estudado.  
- Resumir tópicos complexos como OSPF, EIGRP, ACLs etc.  
- Ajudar na resolução de exercícios.  
- Gerar planos de estudo para iniciantes ou avançados.

### Exemplos de perguntas:

- “Explique o funcionamento do protocolo OSPF.”  
- “Me dê um exemplo de configuração de VLAN e trunk.”  
- “Gere um quiz com 5 questões sobre subnetting.”  
- “Como configuro uma ACL padrão e estendida?”  
- “Resuma o funcionamento do STP.”  

---
## Arquitetura do Projeto

- **Agente Tutor de CCNA** (LLM)
- Console para testes e simulação de conversas
- O usuário pergunta e o agente responde com explicações detalhadas

---
## Fluxo de Funcionamento

flowchart TD

    A[Usuário envia uma pergunta ou pedido<br>Ex: 'Explique OSPF'<br>ou 'Gere um quiz de subnetting'] --> B

    B[Agente Tutor CCNA no AI Foundry<br>Modelo: gpt-4.1-mini] --> C

    C{O agente identifica<br>o tipo de tarefa?}

    C -->|Explicação teórica| D[Gerar explicação didática<br>com exemplos, analogias e diagramas]
    C -->|Resumo / mapa mental| E[Criar resumo estruturado<br>em bullets, tópicos, comparações]
    C -->|Quiz| F[Criar perguntas e respostas + feedback depois de cada resposta do usuário<br>baseado no tema solicitado]
    C -->|Configuração Cisco| G[Gerar comandos IOS válidos<br>com comentários]
    C -->|Correção de exercício| H[Analisar resposta do usuário<br>corrigir e explicar o erro]
    C -->|Plano de estudo| I[Gerar roadmap personalizado<br>baseado no nível do usuário]

    D --> J[Modelo formata a resposta]
    E --> J
    F --> J
    G --> J
    H --> J
    I --> J

    J --> K[Usuário recebe a resposta final<br>em formato claro e didático]

---
## Vídeo(s) demonstrativo(s) contendo:
1. Criação de um grupo de recursos.
2. Criação de um recurso do AI Foundry.
3. O deployment de um modelo.
4. Criação do Agente Tutor.
5. Uso do Agente no Chat Playground para testar como o tutor se comporta.

Azure Frontier Girls Challenge Video 1: https://www.youtube.com/watch?v=VcNyDnDoqek

Azure Frontier Girls Challenge Video 2: https://www.youtube.com/watch?v=d03GA3xGTG0
