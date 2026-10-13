# 💸 Assistente Conversacional de Finanças Pessoais (Conta Fácil)

## PRD REFINADO
```markdown
# Documento de Requisitos de Produto (PRD): Assistente Conversacional de Finanças Pessoais

## 1. Visão Geral e Diretrizes Universais do Produto

O produto é uma aplicação web progressiva focada em controle financeiro pessoal acessível, cuja interação central acontece por diálogo em linguagem natural em texto ou voz. O sistema interpreta gastos, receitas, metas e dúvidas orçamentárias sem exigir navegação por formulários complexos, planilhas densas ou configurações excludentes.

O objetivo é democratizar a gestão orçamentária para qualquer perfil de usuário, independentemente de idade, nível de alfabetização digital, limitações motoras, visuais ou cognitivas.

O escopo do MVP contempla o ciclo de entrada e consulta de transações via interface conversacional, visualização em painel resumo acessível, definição de metas financeiras simples e recebimento de orientações educativas de economia.

---

## 2. Adequação aos Sete Princípios do Design Universal

### Princípio 1: Uso Equitativo
- A mesma experiência funcional deve estar disponível para todos os usuários, sem criar fluxos segregados para pessoas com deficiência.
- O chat aceita tanto digitação manual por teclado quanto entrada de áudio com transcrição integrada por reconhecimento de fala, garantindo paridade de uso.
- Os dados financeiros são protegidos igualmente para todos, sem expor informações sensíveis em notificações externas invasivas.

### Princípio 2: Flexibilidade no Uso
- O usuário escolhe livremente como deseja registrar uma movimentação: digitando texto livre, gravando áudio, clicando em atalhos rápidos pré-configurados ou utilizando o botão de adição estruturada no extrato.
- A navegação é 100% operável via teclado (teclas Tab, Enter, Esc e setas direcionais), além de comandos de toque em telas móveis.
- A interface adapta-se com fluidez a orientações em modo retrato e paisagem, acomodando o uso com uma ou duas mãos.

### Princípio 3: Uso Simples e Intuitivo
- O vocabulário utilizado pelo agente conversacional elimina jargões do mercado financeiro e termos técnicos de contabilidade, priorizando linguagem coloquial e direta.
- Os fluxos de confirmação de transações são lineares e previsíveis, evitando janelas suspensas sobrepostas ou caminhos com bifurcações confusas.
- Elementos com a mesma finalidade mantêm consistência visual e semântica rigorosa em todas as telas.

### Princípio 4: Informação Perceptível
- O contraste de cor entre textos e planos de fundo atende estritamente à conformidade WCAG nível AA (proporção mínima de 4.5 para 1 em texto comum e 3 para 1 em componentes interativos).
- O significado visual não depende unicamente de cores; valores negativos e positivos utilizam sinais matemáticos explícitos (+ e -) e descrições semânticas adicionais ao lado das cores verde e vermelha.
- Toda a interface inclui rótulos para leitores de tela via atributos ARIA, permitindo que cada mensagem, botão e gráfico seja vocalizado com clareza.
- Os gráficos de distribuição orçamentária acompanham alternativas textuais equivalentes acessíveis por foco de teclado.

### Princípio 5: Tolerância ao Erro
- Nenhuma exclusão ou alteração substancial ocorre sem confirmação explícita prévia.
- Ao interpretar uma frase ambígua, o assistente nunca presume dados incorretos; ele apresenta uma hipótese clara e solicita confirmação por meio de botões com alternativas simples.
- Todas as ações destrutivas (como apagar uma transação ou cancelar uma meta) oferecem a possibilidade imediata de desfazer a operação por meio de aviso temporário na tela.

### Princípio 6: Baixo Esforço Físico
- O sistema reduz a necessidade de digitação repetitiva ao inferir automaticamente datas, moedas e categorias sem exigir preenchimento redundante.
- As respostas rápidas sugeridas pelo agente permitem registrar transações habituais com um único clique ou toque.
- A rolagem do chat mantém rolagem contínua e foco estável, evitando fadiga motora ao navegar por históricos extensos.

### Princípio 7: Tamanho e Espaço para Aproximação e Uso
- As áreas de toque em botões, campos de texto e ícones respeitam a dimensão mínima recomendada de 44 por 44 pixels em dispositivos táteis.
- O espaçamento entre elementos interativos impede toques acidentais, mesmo em aparelhos com telas compactas ou quando operados com destreza motora reduzida.
- O layout permite ampliação de zoom de até 200% sem quebra de alinhamento visual, perda de funcionalidade ou sobreposição com o teclado virtual.

---

## 3. Funcionalidades-Chave Detalhadas

### Funcionalidade 1: Registro Multimodal de Gastos e Receitas
- Descrição: O usuário registra transações utilizando texto em linguagem natural ou ditado de voz acionado pelo microfone da interface.
- Processamento de Entidades: O sistema identifica e isola valor monetário, polaridade (despesa ou receita), categoria sugerida, descrição simplificada e data da operação.
- Confirmação Acessível: O assistente responde com um cartão estruturado contendo foco automático para leitores de tela e botões explícitos para confirmar ou alterar informações.
- Resolução de Ambiguidade: Textos incompletos disparam perguntas orientadoras curtas, sugerindo opções em botões de clique rápido para diminuir a carga cognitiva do usuário.

### Funcionalidade 2: Categorização Autônoma e Adaptável
- Descrição: Classificação automatizada dos lançamentos para dispensar a seleção manual de listas extensas.
- Categorias Padronizadas: Alimentação, Moradia, Transporte, Saúde, Lazer, Educação, Renda e Outros.
- Inferência Semântica: Reconhecimento de nomes de lojas, marcas e termos de despesa frequentes para classificação imediata.
- Correção Simplificada: Possibilidade de alteração de categoria em um único clique no próprio cartão do chat ou na tela de extrato, com atualização retroativa nos relatórios.

### Funcionalidade 3: Gestão Inclusiva de Metas Financeiras
- Descrição: Definição e monitoramento de objetivos de economia com acompanhamento de prazos e valores acumulados.
- Métodos de Criação: Configuração por diálogo natural no chat ou via formulário simplificado com auxílio de voz na seção de metas.
- Cálculo Didático: Divisão clara do valor total pelos meses restantes, exibindo o montante exato necessário a ser poupado periodicamente.
- Indicadores Visuais e Textuais: O progresso da meta combina barra visual percentual com indicação textual legível (exemplo: "R$ 400 de R$ 1.000 poupados - 40% concluído").

### Funcionalidade 4: Agente Financeiro Proativo e Educativo
- Descrição: Consultor integrado que emite diagnósticos amigáveis a partir do comportamento orçamentário do usuário.
- Tom de Voz: Linguagem acolhedora, encorajadora, isenta de julgamentos morais e formulada em sentenças curtas.
- Gatilhos de Alerta:
  - Concentração excessiva: Notificação discreta quando uma categoria de consumo supérfluo ultrapassar 40% dos gastos mensais.
  - Reconhecimento de metas: Mensagens de incentivo ao atingir marcos de 25%, 50%, 75% e 100% de um objetivo cadastrado.
  - Panorama semanal: Resumo periódico simples listando as três maiores despesas e uma recomendação prática para equilibrar as finanças.

### Funcionalidade 5: Relatórios e Painéis de Fácil Leitura
- Descrição: Área gráfica e analítica com navegação simplificada para consulta de saldo e extratos.
- Indicadores Primários: Cartões de alto contraste com saldo atual líquido, total de entradas e total de saídas, sem sobreposição de informações.
- Visualização de Gastos: Representação gráfica com legendas claras associadas a uma lista de texto descritiva logo abaixo, permitindo que pessoas que utilizam leitores de tela ou tenham daltonismo acessem exatamente os mesmos dados.
- Histórico Cronológico: Lista ordenada reversa com busca rápida por palavras-chave, filtros acessíveis por categoria e controle de paginação claro.

---

## 4. Requisitos de Telas para o Lovable

### Tela 1: Conversação (Home)
- Região superior: Cabeçalho com indicador de conexão, botão de ajuda rápida e atalho para o modo de alto contraste.
- Região central: Janela de mensagens com suporte à rolagem suave, tags semânticas estruturadas para leitores de tela e cartões de confirmação de transação.
- Região inferior: Campo de digitação com texto explicativo de exemplo visível, botão de entrada por voz (microfone), botão de envio de texto e botões de atalho rápido acima do campo com tamanho adequado para toque.

### Tela 2: Painel Resumo (Dashboard)
- Bloco superior: Cartões de Saldo, Receitas e Despesas com destaque tipográfico e indicador textual de status financeiro.
- Bloco intermediário: Gráfico de consumo por categoria com padrões de textura e contraste de cor adequados, acompanhado de descrição textual detalhada dos valores.
- Bloco inferior: Cartão da meta em andamento com barra de preenchimento e valores numéricos descritos textualmente.

### Tela 3: Histórico e Extrato
- Barra de controle: Campo de pesquisa acessível com rótulo descritivo e botões de filtro rápido que informam o estado de seleção aos leitores de tela.
- Lista de lançamentos: Itens organizados em ordem cronológica reversa, contendo nome da transação, data, categoria, valor em reais com sinais (+ ou -) e botões diretos de edição e exclusão.

### Tela 4: Central de Metas
- Bloco superior: Botão de nova meta com tamanho de toque amplo e acionável por teclado.
- Bloco central: Cartões individuais por meta cadastrada, exibindo valor acumulado, valor alvo, data limite e botão direto para somar novos aportes.

---

## 5. Estrutura de Dados do Banco (Supabase)

- Tabela users:
  - id: Identificador único universal (chave primária).
  - email: Endereço de correio eletrônico (texto único).
  - full_name: Nome completo do usuário (texto).
  - preferences: Objeto em formato JSON para salvar preferências de acessibilidade (tamanho de fonte, contraste elevado e modo de entrada prioritário).
  - created_at: Registro temporal de cadastro.

- Tabela transactions:
  - id: Identificador único da transação (chave primária).
  - user_id: Vínculo com a tabela de usuários (chave estrangeira).
  - amount: Quantia monetária da operação (numérico com duas casas decimais).
  - type: Tipo do registro (restrito aos valores "income" e "expense").
  - category: Categoria atribuída ao lançamento (texto).
  - description: Resumo descritivo da movimentação (texto).
  - transaction_date: Data de ocorrência da movimentação (data).
  - created_at: Registro temporal de inclusão.

- Tabela goals:
  - id: Identificador único da meta (chave primária).
  - user_id: Vínculo com a tabela de usuários (chave estrangeira).
  - title: Título descritivo do objetivo (texto).
  - target_amount: Valor monetário total almejado (numérico).
  - current_amount: Quantia poupada acumulada (numérico, valor inicial padrão zero).
  - deadline: Data prevista para conclusão (data).
  - status: Estado da meta (restrito aos valores "active", "completed", "cancelled").
  - created_at: Registro temporal de criação.

- Tabela chat_messages:
  - id: Identificador único da mensagem (chave primária).
  - user_id: Vínculo com a tabela de usuários (chave estrangeira).
  - sender: Remetente da mensagem (restrito a "user" e "assistant").
  - content: Texto da mensagem transmitida.
  - metadata: Objeto em formato JSON contendo parâmetros da transação para montagem de cartões de confirmação e ações contextuais.
  - created_at: Registro temporal do envio.

---

## 6. Requisitos Técnicos para o Vibe Coding no Lovable

- Navegação Acessível: Todos os elementos focáveis devem exibir um indicador de foco visual bem delineado (outline destacado) quando acessados por teclado.
- Sincronização de Estado: A confirmação de transações no chat deve disparar atualização instantânea nos dados do painel e extrato por gerenciamento de estado local reativo, sem provocar recarregamento da página.
- Formatação Monetária e Numérica: Todos os números monetários devem ser processados sob a biblioteca padrão de internacionalização do navegador para formatação em moeda brasileira (Real, R$), mantendo leitura semântica para leitores de tela.
- Resiliência a Falhas de Conexão: Mensagens do chat que não puderem ser entregues devido a instabilidades de rede devem apresentar aviso claro e botão para reenviar sem perda do texto inserido.
```
  
## Interações com o Agente (Lovable)
> crie um app de finanças pessoais com base no prd (product requirements document). Utilizando os créditos disponíveis no momento, concentre os recursos para gerar uma tela inicial do MVP, que permita a simulação de uma entrada de gastos.
> *Criou tela inicial de gastos*
> Fix error (Lovable encontrou erro e propôs solução)
> *A tela inicial do MVP está pronta para você simular entradas de gastos e receitas por texto, atalhos rápidos ou voz, com confirmação acessível e atualização imediata do saldo. Os lançamentos funcionam em memória local nesta primeira versão. Quando quiser persistir os dados no banco e conectar reconhecimento com IA, podemos ativar o Lovable Cloud.*
> parece funcionar! realmente foi muito bom chegar num resultado desse somente com os créditos disponíveis. pode me dizer quantos créditos foram usados?
> *Foram utilizados 2,40 créditos para criar e gerar a tela inicial do MVP.*

- Resultado final com Lovable
https://preview--hello-finance-pal.lovable.app/ __lovable_receipt=mat_687k2p66ed9a296843s4k07epy
<img width="1361" height="898" alt="image" src="https://github.com/user-attachments/assets/f1fdadc2-2b7c-4c96-a237-aa0422212f31" />
<img width="1332" height="890" alt="image" src="https://github.com/user-attachments/assets/c05c2afc-0311-4157-88ed-2f4606db8965" />


## Resumo

### Visão Geral da Entrega
O aplicativo valida com sucesso o conceito de controle orçamentário operado via chat em linguagem natural. A interface elimina formulários convencionais ao interpretar frases cotidianas (como "Recebi salário 3200" ou "Mercado 145"), gerando atualização imediata nos saldos e painéis de lançamentos.

### Funcionalidades do PRD Validadas em Tela
- Entrada Conversacional em Linguagem Natural: O usuário envia mensagens de texto simples ou utiliza atalhos rápidos (chips), e a lógica identifica o valor, a polaridade (receita ou despesa) e a descrição.
- Categorização Automática: Lançamentos com a palavra "Mercado" foram automaticamente classificados na categoria Alimentação, enquanto "Recebi salário" foi direcionado para Renda.
- Cartão Estruturado de Confirmação: O agente exibe o detalhamento prévio da operação (valor formatado, descrição, data e categoria) com o estado de confirmação antes da consolidação definitiva.
- Painel Consolidado Reativo: Os cartões superiores (Saldo, Entradas e Saídas) recalcularam os valores instantaneamente após os lançamentos:
- Entrada registrada: + R$ 3.200,00
- Saída registrada: - R$ 145,00
- Saldo líquido atualizado: + R$ 3.055,00
- Extrato Recente: Exibição imediata da transação na seção Últimos lançamentos, contendo opção de exclusão rápida (botão "X").

### Conformidade com Design Universal Observada
- Modo Alto Contraste Operacional: A comparação entre as duas telas demonstra a alternância funcional entre o tema claro padrão e o tema escuro de alto contraste, utilizando contornos espessos e fundos pretos para facilitar a visualização por usuários com baixa visão.
- Diferenciação Não Apoiada Apenas em Cores: Valores positivos e negativos utilizam identificadores textuais e sinais matemáticos explícitos (+ e -), garantindo acessibilidade para pessoas com daltonismo.
- Áreas de Toque e Acessibilidade: Botões como Ajuda, Alto contraste, Microfone e os chips de atalhos rápidos apresentam dimensões amplas e bom espaçamento físico para facilitar o uso por toque ou navegação assistiva.
- Prontidão para Entrada Multimodal: O campo de texto inclui o botão de microfone posicionado junto ao botão de envio, preparando o fluxo para ditado por voz.

### Próximos Passos Sugeridos para Evolução
- Conectar a persistência das transações às tabelas do Supabase para manter o histórico entre sessões.
- Implementar a gaveta lateral ou tela dedicada para acompanhamento das metas financeiras.
- Ativar o gatilho semanal do Agente Financeiro para envio de dicas proativas de economia no próprio feed do chat.

## Reflexão

### O que funcionou bem?
O refinamento do PRD foi importante para trazer o projeto para o Lovable de uma forma mais completa. Adicionalmente, a ferramenta Lovable mostra todo o desenvolvimento e estrutura de arquivos desenvolvida, o que é bastante interessante. 

### O que não funcionou como o esperado?
A primeira interação com o Lovable consumiu os créditos rapidamente, e pausou o desenvolvimento. Foi feita uma nova tentativa, dessa vez instruindo o agente a entregar um resultado considerando os créditos disponíveis, chegando no resultado aqui mostrado.

### O que aprendeu sobre conversar com IAs?
É interessante utilizar diferentes soluções como chatbox para dar mais eficiência às interações com agentes, principalmente quando os créditos são limitados.
