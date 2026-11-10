# MeuNegocio.AI-Construindo-um-produto-Digital-com-Agentes-de-IA-e-LOvable
Criação de um apaginapara empresa de Personalizados

Prompt"
# CHARLES PERSONALIZADOS — PROMPT MASTER PARA LOVABLE

## 1. OBJETIVO DO PROJETO

Desenvolva uma plataforma web profissional, responsiva e funcional para a empresa **CHARLES PERSONALIZADOS**, especializada em:

- Papelaria personalizada.
- Reformas e restauração de Bíblias.
- Lembranças cristãs e personalizadas.
- Papelaria no atacado.
- Produtos para igrejas, público evangélico, pequenas empresas e revendedores.

A plataforma deverá possuir duas áreas independentes:

1. **Área pública:** apresentação dos produtos e serviços, catálogo, formulário de contato e canais de atendimento.
2. **Área administrativa privada:** dashboard, cadastro manual de clientes, gerenciamento de contatos, indicadores e configurações.

O objetivo principal é permitir que o proprietário administre o negócio com autonomia, cadastre clientes ativos manualmente e receba uma notificação por e-mail sempre que um novo cliente potencial preencher o formulário de contato.

Não crie apenas uma interface estática. Implemente funcionalidades reais, persistência de dados, autenticação, autorização e integrações de backend.

---

## 2. IDENTIDADE VISUAL

Nome oficial da marca: **CHARLES PERSONALIZADOS**.

Utilize uma identidade visual moderna, profissional, comercial e elegante.

### Paleta de cores

- Laranja principal: `#F97316`
- Cinza: `#6B7280`
- Preto: `#171717`
- Fundo claro: `#F9FAFB`
- Branco: `#FFFFFF`

### Aplicação das cores

- Laranja para botões principais, ações de cadastro, destaques e indicadores.
- Preto para títulos, textos principais e elementos de navegação.
- Cinza para informações secundárias, bordas e elementos auxiliares.
- Branco e fundo claro para melhorar a leitura.

Crie um logotipo tipográfico inicial com o nome CHARLES PERSONALIZADOS, que possa ser substituído posteriormente por uma identidade visual definitiva.

Utilize ícones consistentes, espaçamento adequado, cards elegantes, tabelas organizadas e formulários acessíveis.

A interface deverá funcionar em computadores, tablets e celulares.

---

## 3. ARQUITETURA GERAL

Antes de implementar, inspecione o projeto atual.

Identifique:
- Framework e estrutura de rotas existentes.
- Backend já conectado.
- Banco de dados atual.
- Sistema de autenticação.
- Integrações e configurações já existentes.

Se o projeto já tiver um backend funcional, preserve-o e amplie sua estrutura.

Se ainda não houver backend, utilize o **Lovable Cloud** como infraestrutura principal, aproveitando os recursos disponíveis e adequados ao projeto.

Não crie serviços duplicados sem necessidade.

Organize o código em componentes reutilizáveis, serviços de dados, validações e módulos independentes.

---

## 4. ÁREA PÚBLICA

Criar as seguintes páginas:

### Página inicial
Apresentar a marca CHARLES PERSONALIZADOS, seus produtos e serviços, com chamadas para ação direcionadas ao catálogo e ao formulário de contato.

### Papelaria personalizada
Apresentar agendas, cadernos, planners, marcadores, cartões, kits e outros produtos personalizados.

### Reformas de Bíblias
Apresentar os serviços de reforma, recuperação de capas, encadernação e personalização.

Permitir que o visitante solicite orçamento, informe o serviço desejado e, quando necessário, envie fotografias por um canal seguro.

### Lembranças e atacado
Apresentar lembranças para igrejas, congressos, eventos, empresas e revendedores.

Preparar a estrutura para preços por quantidade, pedidos mínimos e orçamentos personalizados.

### Página de contato
Disponibilizar formulário de contato e botão para atendimento pelo WhatsApp.

Não invente números de telefone, endereço, e-mail ou links comerciais. Esses dados deverão ser configuráveis pelo administrador.

---

## 5. ENGRENAGEM ADMINISTRATIVA NO CANTO SUPERIOR DIREITO

Este requisito é obrigatório.

Adicionar um ícone de engrenagem no canto superior direito do cabeçalho da plataforma.

No desktop, posicionar a engrenagem no extremo direito do cabeçalho. No celular, manter o acesso disponível no cabeçalho ou menu responsivo.

Ao clicar na engrenagem, abrir um menu com a opção:

**Área Administrativa**

Ao selecionar essa opção:
- Direcionar o usuário para `/admin/login`.
- Solicitar autenticação.
- Após o login, abrir o dashboard administrativo em `/admin`.
- Caso não esteja autenticado, impedir o acesso às rotas administrativas.

A engrenagem não deve expor dados, credenciais ou funcionalidades administrativas a visitantes.

A proteção precisa ser implementada no backend, nas rotas e nas políticas de acesso ao banco de dados, não apenas escondendo elementos da interface.

---

## 6. DASHBOARD ADMINISTRATIVO

Criar um dashboard exclusivo para o proprietário da CHARLES PERSONALIZADOS.

### Menu administrativo

- Dashboard.
- Clientes.
- Contatos recebidos.
- Produtos e serviços.
- Pedidos e encomendas.
- Notificações.
- Configurações.
- Sair.

### Indicadores principais

Exibir cards com:

1. Total de clientes ativos.
2. Total de clientes cadastrados.
3. Novos contatos recebidos.
4. Contatos aguardando atendimento.
5. Pedidos em andamento.
6. Total de pedidos registrados.

Os indicadores deverão ser calculados a partir dos dados reais do banco de dados.

Não utilizar números fixos ou fictícios como se fossem dados reais.

### Seção de atividades recentes

Apresentar:
- Últimos clientes cadastrados.
- Últimos contatos recebidos.
- Data e hora de cada contato.
- Status do atendimento.
- Atalhos para visualizar os detalhes.

Criar estados vazios informativos para quando ainda não existirem registros.

---

## 7. CADASTRO MANUAL DE CLIENTES ATIVOS

Inicialmente, o proprietário deverá cadastrar manualmente os clientes que já possui.

Na página `/admin/clientes`, criar um botão destacado:

**+ NOVO CLIENTE**

### Campos do cadastro

- Nome completo ou nome empresarial.
- E-mail.
- Telefone.
- WhatsApp.
- Tipo de cliente:
  - Pessoa física.
  - Igreja ou ministério.
  - Pequena empresa.
  - Revendedor.
- Produtos ou serviços de interesse.
- Status:
  - Ativo.
  - Inativo.
  - Potencial.
- Data do cadastro.
- Observações internas.

### Funcionalidades obrigatórias

- Criar clientes manualmente.
- Editar dados.
- Consultar detalhes.
- Pesquisar por nome, telefone e e-mail.
- Filtrar por tipo e status.
- Alterar o status do cliente.
- Exibir data de criação e última atualização.
- Confirmar ações destrutivas.
- Evitar duplicidades evidentes.
- Atualizar os indicadores do dashboard após alterações.

Os clientes cadastrados manualmente deverão ser salvos no banco de dados e continuar disponíveis após sair e entrar novamente no sistema.

Permitir cadastrar clientes mesmo quando não houver nenhum contato público anterior.

O cadastro de um cliente no painel administrativo não deve exigir que ele crie uma conta ou senha.

---

## 8. FORMULÁRIO PÚBLICO DE CONTATO

Criar um formulário acessível a qualquer visitante, sem exigir login.

### Campos

- Nome.
- E-mail.
- WhatsApp.
- Tipo de interesse:
  - Papelaria personalizada.
  - Reforma de Bíblia.
  - Lembranças.
  - Atacado.
  - Produtos para empresas.
  - Outro.
- Mensagem.
- Consentimento para tratamento dos dados pessoais, com informação sobre a finalidade do contato.

### Processo de envio

Quando o visitante enviar o formulário:

1. Validar os campos no frontend e no backend.
2. Validar e normalizar os dados.
3. Aplicar proteção contra spam e envios abusivos.
4. Salvar o contato no banco de dados.
5. Gerar um identificador único.
6. Registrar data e hora.
7. Definir o status inicial como `novo`.
8. Acionar a notificação por e-mail no backend.
9. Atualizar a área administrativa.
10. Exibir uma mensagem de confirmação ao visitante após a gravação bem-sucedida.

Mensagem sugerida:

“Obrigado por entrar em contato com a CHARLES PERSONALIZADOS! Recebemos sua mensagem e entraremos em contato assim que possível.”

A mensagem só deverá aparecer como confirmação de recebimento quando os dados tiverem sido salvos com sucesso.

### Tratamento de falhas

Se o envio do e-mail falhar:
- Não apagar o contato.
- Manter o registro disponível no dashboard.
- Registrar a falha da notificação.
- Permitir que o administrador tente enviar novamente.

Evitar a criação de registros duplicados durante novas tentativas técnicas.

O formulário público não deve permitir que o visitante consulte contatos de terceiros, altere registros ou acesse observações administrativas.

---

## 9. ALERTA AUTOMÁTICO POR E-MAIL

Implementar o envio de uma notificação sempre que um novo contato for salvo com sucesso.

Utilizar uma função de backend segura e um provedor de e-mail transacional compatível, como Resend, se disponível e configurado.

O destinatário administrativo deverá ser configurado nas configurações do sistema.

### Assunto do e-mail

**Novo contato recebido — CHARLES PERSONALIZADOS**

### Conteúdo do e-mail

- Nome do contato.
- E-mail.
- WhatsApp.
- Tipo de interesse.
- Mensagem enviada.
- Data e hora.
- Identificador do contato.
- Link para visualizar o contato no dashboard administrativo.

O e-mail deverá ter um layout HTML responsivo, usando a identidade visual da empresa: laranja, cinza, preto e branco.

Incluir um botão “Ver contato no painel”.

O link deverá direcionar para a rota administrativa correta, sem inserir dados pessoais ou credenciais na URL.

### Requisitos de segurança

- Enviar e-mails somente pelo backend.
- Armazenar a chave do provedor em secrets seguros.
- Não expor chaves de API no frontend.
- Validar o destinatário configurado.
- Registrar o status de cada envio.
- Implementar controle de tentativas e reenvio.
- Evitar notificações duplicadas causadas por repetição do mesmo evento.
- Registrar erros sem armazenar segredos ou dados sensíveis desnecessários.

Criar uma tela de configurações para informar ou alterar o e-mail administrativo.

Se o serviço de e-mail não estiver configurado, mostrar claramente no painel que a configuração está pendente.

Não afirmar que o e-mail foi enviado sem confirmação do provedor.

---

## 10. UTILIZAÇÃO DOS RECURSOS LOVABLE CLOUD

Utilizar os recursos disponíveis do Lovable Cloud que agreguem valor real ao sistema.

### Banco de dados
Armazenar clientes, contatos, configurações, produtos, pedidos e registros de notificações de forma persistente.

### Autenticação
Utilizar o mecanismo de autenticação suportado pelo backend existente ou pelo Lovable Cloud.

Implementar login, logout, recuperação de acesso quando suportada e proteção de rotas.

### Autorização
Separar permissões públicas e administrativas.

Não permitir que usuários comuns se tornem administradores por meio de cadastro público.

### Funções de backend
Implementar funções seguras para:
- Processar formulários.
- Validar dados.
- Disparar notificações.
- Realizar operações administrativas autorizadas.
- Registrar falhas e eventos importantes.

### Armazenamento de arquivos
Preparar o armazenamento para imagens dos produtos, fotografias de referência e outros arquivos necessários.

Utilizar permissões adequadas. Fotografias ou documentos privados não devem ficar acessíveis publicamente sem autorização.

### Secrets e variáveis de ambiente
Centralizar credenciais e chaves de serviços externos no mecanismo seguro de secrets do backend.

Nunca colocar chaves privilegiadas no código enviado ao navegador.

### Atualizações em tempo real
Quando suportado e apropriado, atualizar os contatos e indicadores do dashboard em tempo real. Caso não seja necessário, utilizar atualização por consulta sem prejudicar o desempenho.

### Logs e monitoramento
Registrar erros de backend, falhas de notificação e eventos administrativos importantes.

### Integrações
Preparar a arquitetura para integrações futuras com:
- Provedor de e-mail.
- WhatsApp.
- Plataforma de pagamentos.
- Plataforma de loja virtual.
- Ferramentas de análise de uso.
- Serviços de inteligência artificial, quando houver um caso de uso concreto.

Não ativar integrações sem necessidade, não inventar credenciais e não declarar que uma integração está funcional sem testar.

---

## 11. ESTRUTURA DO BANCO DE DADOS

Criar tabelas com identificadores únicos, datas de criação e atualização e relacionamentos adequados.

### Tabela `clients`

Campos:
- `id`
- `full_name`
- `email`
- `phone`
- `whatsapp`
- `client_type`
- `interests`
- `status`
- `internal_notes`
- `created_at`
- `updated_at`

### Tabela `contact_requests`

Campos:
- `id`
- `name`
- `email`
- `phone`
- `interest_type`
- `message`
- `privacy_consent`
- `status`
- `created_at`
- `updated_at`

### Tabela `notification_logs`

Campos:
- `id`
- `contact_request_id`
- `channel`
- `recipient`
- `status`
- `provider_message_id`
- `attempt_count`
- `error_message`
- `sent_at`
- `created_at`

### Tabela `admin_profiles`

Campos:
- `id`, vinculado ao identificador do usuário autenticado.
- `display_name`
- `email`
- `role`
- `created_at`
- `updated_at`

Não armazenar senhas manualmente nas tabelas.

### Tabela `app_settings`

Campos:
- `id`
- `setting_key`
- `setting_value`, com proteção de acesso apropriada.
- `updated_at`

Utilizar essa estrutura apenas para configurações não secretas ou dados protegidos adequadamente. Chaves de API e credenciais devem ficar no armazenamento de secrets do backend.

Preparar o modelo para futuras tabelas de produtos, categorias, pedidos, itens de pedido, serviços de reforma e auditoria.

---

## 12. SEGURANÇA E LGPD

Implementar políticas de Row Level Security (RLS) quando suportadas pelo banco utilizado.

Regras obrigatórias:

- Somente administradores autorizados podem consultar a lista completa de clientes.
- Somente administradores autorizados podem consultar todos os contatos recebidos.
- Visitantes podem enviar contatos por uma operação pública controlada.
- Visitantes não podem listar, editar ou excluir contatos.
- Apenas administradores autorizados podem alterar status, editar clientes e acessar observações internas.
- A autorização deve ser verificada no backend.
- Nenhuma chave privilegiada deve ser exposta no navegador.
- O primeiro administrador deverá ser criado por um processo seguro.
- O cadastro público não poderá conceder privilégios administrativos.
- Implementar validação de entrada, limites de requisição e tratamento seguro de erros.
- Coletar somente os dados pessoais necessários.
- Informar a finalidade da coleta e implementar medidas adequadas de proteção dos dados.

Criar um registro de auditoria para ações administrativas relevantes, respeitando a necessidade e a minimização de dados.

---

## 13. PRODUTOS E PEDIDOS

Preparar o painel para permitir o gerenciamento futuro de produtos e serviços.

### Produtos
- Nome.
- Categoria.
- Descrição.
- Imagem.
- Preço.
- Disponibilidade.
- Tipo de venda: varejo, atacado ou orçamento.
- Quantidade mínima, quando aplicável.

### Pedidos
- Cliente associado, quando existente.
- Produtos ou serviços solicitados.
- Quantidades.
- Valor total.
- Status do pedido.
- Data do pedido.
- Prazo previsto.
- Observações administrativas.

Os pedidos deverão ser persistidos no banco de dados e protegidos por autorização.

Não implementar pagamentos reais ou afirmar que pedidos estão pagos sem uma integração de pagamento configurada e validada.

---

## 14. CONFIGURAÇÕES ADMINISTRATIVAS

Criar uma página de configurações que permita gerenciar:

- Nome da empresa.
- E-mail de notificação.
- WhatsApp comercial.
- Instagram comercial.
- Informações institucionais.
- Horário de atendimento.
- Preferências de notificação.
- Estado da integração de e-mail.

Os campos deverão ser editáveis pelo administrador autorizado.

Exibir claramente quais integrações estão ativas, pendentes ou com falha.

Não exibir credenciais secretas no painel.

---

## 15. QUALIDADE DA INTERFACE

A aplicação deve ter:
- Navegação intuitiva.
- Design consistente com a marca.
- Tabelas com pesquisa e filtros.
- Paginação quando necessária.
- Formulários com validação.
- Mensagens de sucesso e erro.
- Indicadores de carregamento.
- Estados vazios informativos.
- Layout adaptado a celulares.
- Contraste e acessibilidade adequados.

O dashboard deverá priorizar informações administrativas, não conteúdo promocional.

A engrenagem administrativa deverá permanecer visível e fácil de localizar na área pública.

---

## 16. TESTES OBRIGATÓRIOS

Executar testes para confirmar:

1. O visitante consegue enviar um formulário sem criar uma conta.
2. O contato é salvo corretamente no banco.
3. O sistema gera um identificador único.
4. O backend aciona a notificação por e-mail.
5. A falha do provedor não apaga o contato.
6. O administrador consegue entrar com autenticação segura.
7. O administrador consegue cadastrar clientes manualmente.
8. Os clientes ativos aparecem no dashboard.
9. Os indicadores são atualizados com dados reais.
10. Os visitantes não conseguem acessar dados administrativos.
11. As políticas RLS impedem acessos indevidos diretamente à API.
12. As chaves secretas não aparecem no frontend.
13. O layout funciona em computadores e celulares.
14. Os erros ficam registrados para investigação.
15. O reenvio de notificações funciona sem criar contatos duplicados.

Corrigir os problemas encontrados antes de considerar a implementação concluída.

---

## 17. ORDEM DE IMPLEMENTAÇÃO

Implemente em etapas, mantendo o projeto funcional:

**Etapa 1 — Infraestrutura**
- Inspecionar o projeto.
- Configurar ou preservar o backend.
- Criar as tabelas.
- Implementar autenticação, autorização e políticas de segurança.

**Etapa 2 — Administração**
- Criar a engrenagem no cabeçalho.
- Criar login administrativo.
- Criar dashboard.
- Implementar cadastro manual de clientes.
- Implementar pesquisa, filtros e indicadores.

**Etapa 3 — Contatos e e-mail**
- Criar formulário público.
- Salvar contatos no banco.
- Configurar o provedor de e-mail.
- Implementar notificações, logs e reenvio.
- Testar o fluxo completo.

**Etapa 4 — Catálogo e expansão**
- Implementar produtos e serviços.
- Preparar pedidos e encomendas.
- Configurar armazenamento de imagens.
- Preparar integrações futuras.

**Etapa 5 — Validação final**
- Executar testes.
- Corrigir erros.
- Verificar permissões.
- Confirmar responsividade.
- Documentar as configurações pendentes.

## 18. ENTREGA FINAL

Ao terminar, apresente um relatório contendo:

- Funcionalidades implementadas.
- Tabelas criadas.
- Recursos do Lovable Cloud efetivamente utilizados.
- Políticas de segurança configuradas.
- Integração de e-mail e resultado dos testes.
- Secrets e configurações que ainda precisam ser preenchidos.
- Testes executados e seus resultados.
- Limitações conhecidas.
- Próximas melhorias recomendadas.

**Critério de conclusão:** a CHARLES PERSONALIZADOS deverá possuir uma área pública funcional, uma área administrativa protegida, cadastro manual de clientes persistente, dashboard alimentado por dados reais e formulário de contato integrado a uma notificação por e-mail pelo backend.

Não entregar apenas uma demonstração visual. Implementar e validar as funcionalidades reais, respeitando as capacidades e configurações disponíveis no projeto Lovable.

----------------------------------------------------------------
https://charlespersonalizados.lovable.app
--------------------------------------------------
