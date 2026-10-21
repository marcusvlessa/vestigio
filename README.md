<div align="center">
  <img src="docs/media/logo.png" alt="Vestígio" width="96" />
  <h1>Vestígio</h1>
  <p><strong>Assistente de análise forense para o IPED: instala, configura, analisa com IA local auditada e entrega o relatório no modelo da sua instituição.</strong></p>
  <p>
    <a href="https://github.com/marcusvlessa/vestigio/releases/latest">Baixar</a> ·
    <a href="#instalar-numa-estação-windows">Instalar</a> ·
    <a href="#vestígio">O painel</a> ·
    <a href="#autorização-de-uso">Autorização de uso</a> ·
    <a href="#desenvolvedor">Desenvolvedor</a>
  </p>
  <p>
    <a href="https://github.com/marcusvlessa/vestigio/releases/latest"><img src="https://img.shields.io/github/v/release/marcusvlessa/vestigio?label=vers%C3%A3o" alt="Versão mais nova" /></a>
    <a href="https://github.com/marcusvlessa/vestigio/releases"><img src="https://img.shields.io/github/downloads/marcusvlessa/vestigio/total?label=downloads" alt="Downloads" /></a>
    <img src="https://img.shields.io/badge/Windows%20%7C%20Linux-0d2f57" alt="Windows e Linux" />
    <img src="https://img.shields.io/badge/IPED-4.3.1-c9a227" alt="IPED 4.3.1" />
    <img src="https://img.shields.io/badge/licen%C3%A7a-GPLv3-blue" alt="GPLv3" />
  </p>
</div>

![Um passeio pelo painel: visão do caso, rede de vínculos, análise financeira, assistente de IA e relatório técnico](docs/media/vestigio.gif)

<p align="center"><sub>Todos os dados das telas são fictícios.</sub></p>

## Do vestígio ao relatório

| Preparar | Analisar | Concluir |
| :--- | :--- | :--- |
| Instala e configura o IPED sozinho, com backup | Visão do caso, rede de vínculos e telemática | Relatório no modelo da instituição (.docx) |
| Processa evidências em fila, com progresso ao vivo | Análise financeira (SIMBA, RIF, extratos) | IA local com log de auditoria por caso |

<details>
<summary><strong>Ver as telas</strong> · visão do caso, rede, financeiro, assistente, relatório e autorização</summary>

<table>
  <tr>
    <td><img src="docs/media/visao.png" alt="Visão do caso" width="100%" /></td>
    <td><img src="docs/media/rede.png" alt="Rede de vínculos" width="100%" /></td>
  </tr>
  <tr><td align="center">Visão do caso</td><td align="center">Rede de vínculos</td></tr>
  <tr>
    <td><img src="docs/media/telematica.png" alt="Registros telemáticos" width="100%" /></td>
    <td><img src="docs/media/dashboard-financeiro.png" alt="Dashboard financeiro" width="100%" /></td>
  </tr>
  <tr><td align="center">Registros telemáticos</td><td align="center">Dashboard financeiro (funciona sem internet)</td></tr>
  <tr>
    <td><img src="docs/media/financeiro.png" alt="Análise financeira com alertas e pergunta à IA" width="100%" /></td>
    <td><img src="docs/media/assistente.png" alt="Assistente de IA" width="100%" /></td>
  </tr>
  <tr><td align="center">Análise financeira</td><td align="center">Assistente de IA</td></tr>
  <tr>
    <td><img src="docs/media/relatorio.png" alt="Relatório técnico" width="100%" /></td>
    <td><img src="docs/media/autorizacao.png" alt="Pedido de autorização de uso" width="100%" /></td>
  </tr>
  <tr><td align="center">Relatório técnico</td><td align="center">Autorização de uso</td></tr>
</table>

</details>

**Vestígio: assistente de análise para o IPED.** Instala e configura o
[IPED](https://github.com/sepinf-inc/IPED) sozinho, conduz o analista por todo o fluxo num painel
local, liga uma IA local com auditoria pelo MCP e gera o relatório no modelo da instituição. Nasceu
na Polícia Civil da Bahia e serve a qualquer instituição de segurança: polícias civis e federais,
perícias, núcleos de inteligência e Ministério Público. O núcleo do IPED não é alterado: tudo aqui
atua sobre os arquivos de configuração, perfis e scripts que o próprio IPED já prevê.

**Baixe a versão mais recente em [Releases](https://github.com/marcusvlessa/vestigio/releases/latest)**
(`iped-pcba-windows.zip` para as estações, `iped-pcba-linux.tar.gz` para o servidor) e dê dois
cliques em `Vestigio.exe` (ou em `instalar.bat`).

O que já funciona:

- **Instalação automática**: se a máquina não tem IPED, o instalador baixa o oficial e confere o
  SHA-256; o painel instala o que faltar (plugins de transcrição e faces, Visual C++, CUDA,
  Ollama, modelo de IA local, leitor de PDF e MCP).
- **Vestígio** no navegador, que conduz o analista por todo o fluxo: configurar a máquina,
  processar evidências (com fila de vários casos e progresso da indexação ao vivo), casos,
  visão do caso, assistente de IA e relatório técnico.
- **Rede de vínculos** completa, com arrasto, zoom e formatos força, circular, hierarquia,
  radial e grade.
- **Multicasos**: abre vários casos juntos no IPED e cruza os contatos entre eles.
- **IA com auditoria**: MCP do IPED (pasta [`mcp/`](mcp/README.md)) com log encadeado por hash,
  IA local por padrão (Ollama ou LM Studio) e ligação opcional ao Claude, Antigravity e Hermes.
- **Skills de análise**: financeira, imagens, áudio, geolocalização, mídias x logs e a análise
  forense completa, instaláveis no Claude Code, no Hermes, no Claude Desktop e na IA local.
- **Análise financeira**: importa SIMBA, RIF do COAF e extratos para uma base do caso, com alertas
  por regra, contrapartes, rede e dashboard sem internet; a IA lê pelo MCP e há um pacote opcional,
  pseudonimizado, para o Google BigQuery e o Looker Studio.
- **Relatórios no modelo de cada instituição**, gerados em `.docx`: Relatório Técnico da Polícia
  Civil (padrão), Laudo Pericial, Relatório de Inteligência e Genérico, todos editáveis no painel.
- **Assistente de IA que mostra o andamento**: "ainda pensando" com contador, erro com o motivo e
  "Finalizado" ao entregar; se a porta do LM Studio estiver ocupada, o painel libera sozinho.
- **Transcrição de áudio** com Whisper large-v3 turbo na GPU.

## Para quem é

Qualquer analista de uma instituição de segurança, em qualquer máquina, com ou sem o IPED já instalado. O
instalador não traz nada fixo de um computador: ele descobre onde está o IPED, que hardware a
máquina tem e o que já está instalado, e configura a partir disso.

## Instalar numa estação Windows

1. Baixe o `iped-pcba-windows.zip` da página de Releases e descompacte em qualquer pasta.
   (O "Download ZIP" do código também serve, mas sem o MCP, que precisa ser compilado.)
2. Dê dois cliques em `Vestigio.exe` (o ícone do escudo). Ele acha o IPED e abre o
   **Vestígio** no navegador, sem janela preta: enquanto o painel roda, fica um ícone perto
   do relógio do Windows, com **Abrir o painel no navegador** e **Encerrar o painel**.
3. Siga os passos do painel.

O `Vestigio.exe` faz o mesmo que o `instalar.bat` e repassa as mesmas opções. Se o painel não abre
ou fecha com erro, ele mostra as últimas mensagens e oferece abrir de novo pelo `instalar.bat`, com
a janela de mensagens (é lá que aparece, por exemplo, a pergunta para baixar o IPED). Com
`-Texto`, `-Simular`, `-Aplicar`, `-Reverter` ou `-Json` ele abre direto o `instalar.bat` no
console. O `instalar.bat` continua no pacote e funciona como antes.

Não precisa instalar Python nem nada: o painel usa o Python que vem dentro do IPED (ou o da máquina,
se houver). Quem acha o IPED, escolhe a versão mais nova e instala o que falta é o mesmo pacote do
painel; o `instalar.ps1` só procura um Python e passa a palavra a ele. Quem abre pelo
`instalar.bat` precisa deixar a janela preta aberta enquanto o painel estiver em uso; pelo
`Vestigio.exe` não há janela.

Se a máquina não tem IPED, o `instalar.bat` oferece baixar a última versão oficial do IPED (cerca de 700 MB)
da página de Releases do projeto IPED, confere o SHA-256 informado pelo GitHub e instala em
`C:\Tools\IPED` (ou no disco com mais espaço). Depois, no passo 1 do painel, o cartão
**O que esta máquina precisa** mostra o que falta e instala com um clique ou com
**Instalar o que falta**:

| Item | Como instala |
|---|---|
| IPED | baixa a última versão oficial com Java e Python, confere tamanho e SHA-256 |
| Transcrição (Whisper) e reconhecimento facial | pacote oficial de plugins do IPED; guarda cópia da pasta `conf` antes e mantém a configuração de transcrição |
| Visual C++ 2015-2022 | instalador da Microsoft em modo silencioso (pede confirmação do Windows) |
| CUDA para o Whisper | só aparece com placa NVIDIA; usa o `whisper_gpu.ps1` |
| Ollama e modelo de IA local | instalador oficial do Ollama e `ollama pull` do modelo indicado pela memória da máquina |
| Leitor de PDF (Poppler) | baixa o `pdftotext` para `%USERPROFILE%\.iped-pcba\poppler` |
| MCP do IPED | copia do pacote da última versão deste projeto |

Pelo console: `python -m iped_pcba.dependencias situacao` e
`python -m iped_pcba.dependencias instalar tudo`.

## Vestígio

Página local (só em `127.0.0.1`, com código de acesso aleatório na URL). O topo mostra o
**caso em análise**, escolhido uma vez e usado em todas as telas. A tela **Início** diz qual é o
próximo passo e mostra o andamento. O menu segue o trabalho:

| Grupo | Tela | O que faz |
|---|---|---|
| Preparar | 1. Configurar a máquina | Mostra o hardware e a configuração proposta, com o valor atual e o motivo de cada item. Dá para desmarcar ou editar qualquer valor antes de aplicar. Aplica com backup, restaura qualquer backup, instala o `faster-whisper` com um clique e cria um atalho do painel na Área de Trabalho. |
| Preparar | 2. Processar evidência | Escolhe evidências, pasta do caso e perfil (em cartões que explicam quando usar cada perfil, o que liga, o que desliga e quanto demora) e roda o IPED. Durante a indexação mostra percentual, itens processados, velocidade, tempo restante, hora prevista de término, as tarefas que cada processo está executando, avisos e erros. Em máquina com placa NVIDIA, confirma se a GPU foi ativada e, se não foi, diz o motivo e oferece corrigir e recomeçar (veja "Confirmação da GPU"). A **fila** processa vários casos em sequência e pode salvar o grupo para a análise multicasos. Ela fica gravada: se o painel fechar ou se atualizar no meio, os casos continuam na fila e o que estava rodando retoma de onde o IPED parou (**Retomar a fila**). |
| Analisar | 3. Casos | Lista os casos, abre no IPED, escolhe o caso em análise e mostra o log de auditoria da IA com a conferência da cadeia de hashes. |
| Analisar | Visão do caso | Gráficos, alertas e sugestões do caso (veja abaixo). |
| Analisar | Análise financeira | Importa SIMBA, RIF e extratos, mostra alertas e abre o dashboard financeiro; gera o pacote opcional do BigQuery (veja abaixo). |
| Analisar | Assistente de IA | Agentes prontos que mandam a pergunta à IA local pelo próprio painel (veja abaixo). |
| Analisar | Multicasos | Seleciona dois ou mais casos (ou um grupo salvo), abre todos juntos no IPED (`-multicases`) e cruza os contatos: quem aparece em mais de um caso, se é titular em algum, e uma rede única colorida por caso. O relatório do cruzamento é salvo em Markdown. |
| Concluir | 4. Relatório técnico | Monta o relatório do caso no modelo escolhido e gera o `.docx` (veja abaixo). |
| Sistema | Conexões de IA (MCP) | Liga e desliga a escrita da IA no caso, liga o MCP ao Claude Desktop, ao Antigravity, ao LM Studio e ao Hermes Agent (com cópia do arquivo antes de alterar), procura Ollama e LM Studio na máquina e testa o MCP com o caso ativo. |

### Assistente de IA

Oito agentes, cada um com seu papel, as ferramentas do MCP que pode usar e perguntas prontas:
Triagem inicial, Comunicações, Financeiro, Linha do tempo, Localização, Mídias e detecções,
Marcação no caso e Redator do RT (os dois últimos escrevem no caso e precisam da escrita
liberada). O texto entre `[COLCHETES]` numa pergunta é para trocar antes de enviar.

**Enviar para a IA local** manda a pergunta ao Ollama ou ao LM Studio desta máquina (o painel
recusa qualquer endereço que não seja `127.0.0.1` ou `localhost`). A IA consulta o caso pelo MCP
e o painel mostra cada passo e o texto da resposta enquanto a IA ainda está escrevendo; toda
chamada fica no log de auditoria do caso. A resposta pode ser
copiada ou salva em `<caso>\iped-pcba-ia\conversas\`. O modelo precisa aceitar ferramentas
(por exemplo qwen2.5, qwen3, llama3.1 ou mistral-nemo).

**Arquivos de contexto**: na mesma tela, anexe arquivos ou pastas de fora do IPED (BO, portaria,
ofícios, depoimentos, relatórios anteriores, planilhas) para a IA entender o caso e cruzar com o
que acha no IPED. Lê `.txt`, `.md`, `.csv`, `.json`, `.html`, `.xml`, `.eml`, `.rtf`, `.docx`,
`.odt`, `.ods`, `.xlsx`, `.pptx` e, com o `pdftotext` instalado, `.pdf`. A lista fica em
`<caso>\iped-pcba-ia\contexto.json` (só os caminhos; nada é copiado). Se o texto é curto, vai junto
com a pergunta; se é longo, a IA busca e lê por ferramentas do próprio painel. A conversa salva
registra o SHA-256 de cada arquivo lido.

**Preparar para Claude e outras IAs** junta o texto dos arquivos de contexto em
`<caso>\iped-pcba-ia\contexto-para-ia.md` para anexar ou colar no Claude (ou outra IA) e em
`contexto-texto.json`, que a ferramenta `case_context_files` do MCP lê. Assim o Claude Desktop
ligado ao MCP busca e lê os mesmos documentos que a IA local. O painel avisa antes que o texto
vai para a nuvem e registra cada preparação e cópia em `contexto-preparado.log`.

**Skills de análise**: seis skills no formato Agent Skills (`skills/`): análise financeira
(PDFs, extratos, SIMBA, RIF), imagens, áudio, geolocalização, mídias x logs de uso do telefone e
a análise forense completa, que orquestra as demais. O cartão **Skills de análise** instala em
`~/.claude/skills` (Claude Code), em `~/.hermes/skills` (Hermes Agent) e gera os `.zip` para
enviar no Claude Desktop ou claude.ai. Cada skill também aparece como agente no painel, para a IA
local. Pelo console: `python -m iped_pcba skills --instalar`.

**Copiar para Claude/Antigravity/Hermes** copia as instruções do agente e a pergunta para colar
no programa ligado ao MCP. Claude Desktop e Antigravity usam modelos na nuvem: o painel avisa
antes de ligá-los, e dados reais devem ficar na IA local.

Depois de aplicar, o painel fica dentro do IPED: `<IPED>\pcba\painel-pcba.bat` abre de novo,
mesmo que a pasta baixada seja apagada. Pelo console: `python -m iped_pcba painel`.

O `instalar.bat -Texto` faz só a configuração pelo console, como antes (pergunta S/N).
Tudo o que o instalador escreve no console fica em `%TEMP%\iped-pcba-instalar.log`.

## Análise financeira

A tela **Análise financeira** importa arquivos ou pastas inteiras:

- **SIMBA**: os arquivos da exportação (Extrato, Contas, Titulares...), separados por tabulação, com
  as colunas do leiaute do Banco Central (`DATA_LANCAMENTO`, `VALOR_LANCAMENTO`, `NATUREZA_LANCAMENTO`,
  `CPF_CNPJ_OD`, `NOME_PESSOA_OD`...). O arquivo de Contas é usado para achar o titular de cada conta.
- **RIF do COAF**: `Comunicacoes.csv`, `Envolvidos.csv` e `Ocorrencias.csv` do SISCOAF, como chegam
  (ponto e vírgula, Windows-1252, legenda dos campos e hash no fim). O painel lê o segmento de cada
  comunicação (nas do SFN, CampoB é o crédito e CampoC o débito), resume o RIF por segmento, por ano e
  por ocorrência, e junta as pessoas citadas com seus papéis, comunicações e marcas de PEP e servidor.
- **Extratos**: qualquer CSV, TXT ou `.xlsx` com colunas de data e valor (o painel acha o cabeçalho
  mesmo com linhas de apresentação antes, entende `1.234,56`, valores negativos e colunas de crédito e
  débito separadas).

Tudo vai para `<caso>\iped-pcba-financeiro\financeiro.sqlite`, com o SHA-256 de cada arquivo lido.
O painel grava a análise em `financeiro.json` e `transacoes.tsv` (lidos pela ferramenta
`financial_analysis` do MCP, para o Claude, o Hermes e a IA local) e o dashboard
`dashboard-financeiro.html`, que abre sem internet: indicadores, alertas, fluxo mensal, saldo acumulado
no período por conta, transações por faixa de valor, contrapartes, tipos de operação, rede financeira,
tabelas filtráveis, RIF (valores por ano, pessoas com mais valor comunicado, linha do tempo das
comunicações) e arquivos importados. O **mapa das comunicações** marca no Brasil a cidade da agência de
cada comunicação do RIF (círculo maior = mais valor) e pinta os estados pelo valor; os contornos e as
coordenadas dos 5.570 municípios vão no próprio pacote (`instalador/iped_pcba/dados`, do IBGE via
kelvins/municipios-brasileiros, licença MIT), então nada é consultado na internet. O saldo acumulado é
créditos menos débitos desde o primeiro lançamento importado, não o saldo do banco.

| Alerta | Quando aparece |
|---|---|
| Possível fracionamento | 3 ou mais operações entre R$ 8.000 e R$ 9.999,99 na mesma conta em 7 dias |
| Conta de passagem | crédito de R$ 10 mil ou mais que sai em pelo menos 80% em até 2 dias |
| Contraparte no RIF, PEP | CPF/CNPJ da contraparte entre os envolvidos do RIF (ou marcado como PEP) |
| Espécie | depósitos em dinheiro e saques |
| Valores redondos | o mesmo valor múltiplo de R$ 1.000 em 5 ou mais transações |
| Criptoativos | transações com corretoras (Binance, Mercado Bitcoin, Foxbit...) |
| Concentração | uma contraparte com mais de 30% do volume |
| RIF: espécie | comunicações do segmento SFN - Espécie |
| RIF: fracionamento, débito imediato, beneficiário oculto | enquadramento da ocorrência citado pelo comunicante |
| RIF: PEP, servidor público | envolvidos com essas marcas |
| RIF: pessoas em várias comunicações | o mesmo CPF/CNPJ em 3 ou mais comunicações |

**Google BigQuery (opcional)**. É nuvem do Google, então o painel não envia nada sozinho. O botão
"Gerar o pacote" grava em `iped-pcba-financeiro\bigquery\` os CSVs, os esquemas, as views dos
dashboards (`views.sql`), o script `carregar.bat`/`carregar.sh` (usa o `bq` do Google Cloud SDK) e
links do Looker Studio já ligados em cada view. No modo **pseudonimizado** (padrão), nomes, CPF/CNPJ,
contas, descrições, nomes de arquivo e o nome do caso viram códigos; a tabela de volta
(`pseudonimos-NAO-ENVIAR.csv`) e a chave ficam só na pasta do caso. O modo **institucional** leva dado
real e só funciona com o projeto Google Cloud da instituição e o número da autorização da instituição.
Cada geração e envio ficam em `bigquery-envios.log`. Com o conector do BigQuery autorizado no Claude,
ele pode rodar `views.sql` e montar os gráficos a partir das views.

Pelo terminal: `python -m iped_pcba financeiro importar --caso <caso> <arquivos ou pastas>` e
`python -m iped_pcba financeiro bigquery --caso <caso> --projeto <projeto>`.

## Visão do caso

O botão "Atualizar números do caso" roda o MCP em modo de exportação
(`iped-pcba-mcp --case <caso> --exportar-visao`), que só lê o índice do IPED e grava
`<caso>\iped-pcba-painel\visao.json`. Os registros telemáticos importados no passo 5 ficam em
`<caso>\iped-pcba-painel\telematica.json`. Nada sai da máquina e os gráficos funcionam sem
internet.

Alertas e sugestões são regras fixas, cada uma com a fonte do número; não são conclusões:

| Alerta | Quando aparece |
|---|---|
| Base de hashes de alerta, CSAM | qualquer item em `hashDb:status=alert` ou no filtro CSAM do IPED (nível alto) |
| Log de auditoria da IA adulterado | a cadeia de hashes do log não confere (nível alto) |
| Armas, drogas, carteiras de criptomoeda | filtros de IA do IPED com itens |
| Arquivos criptografados | categoria de criptografados com itens |
| Pico de atividade | mês acima de média + 2 desvios e de 3x a mediana dos meses |
| Apagados e carving | itens `deleted:true` e `carved:true` |
| Contato dominante | um contato com 35% ou mais das interações dos mais ativos |
| Madrugada | 25% ou mais dos registros telemáticos entre 0h e 6h |
| Conta em vários dispositivos | a mesma conta com mais de um dispositivo nos registros |
| RT escrito pela IA | campos marcados para revisão no rascunho |

A **rede de vínculos** mostra todos os vínculos do caso (não só os primeiros). Dá para arrastar
os contatos, mover e dar zoom na tela, escolher o formato (força, circular, hierarquia, radial ou
grade), a quantidade de vínculos, os nomes visíveis e a cor por tipo ou por grupo, buscar um
contato, abrir em tela cheia e baixar a imagem em SVG.

As sugestões apontam o próximo passo (criar marcadores, transcrever áudios, ativar faces,
importar telemática, pedir cadastro de IPs, completar o RT, ligar a IA) e várias trazem uma
pergunta pronta para copiar e colar no programa de IA ligado ao MCP.

## Relatório técnico (RT) e outros modelos

Cada caso escolhe o modelo do relatório no card "Modelo do relatório". Vêm prontos o Relatório
Técnico da Polícia Civil (padrão), o Laudo Pericial, o Relatório de Inteligência e o Genérico. Para
adaptar à sua instituição, duplique um deles e edite cabeçalho, logo, tarja, capa, qualificação e
seções no próprio painel (formulário ou JSON, com validação); os modelos próprios ficam em
`~\.iped-pcba\modelos-relatorio\`, e o padrão para casos novos fica nos dados da unidade.

No modelo padrão, o passo 5 do painel monta o RT na estrutura do modelo institucional: capa, bloco de qualificação,
apresentação, objetivo, fatos e relações, cadastro telefônico, terminais improdutivos, uma análise
por provedor (tabela INVESTIGADO | CONTA | PERÍODO, texto, quadros e conclusão), metodologia (IPED,
MD5, SHA-256), providências e assinaturas, com cabeçalho institucional e rodapé SIGILO LEGAL em
todas as páginas. O que estiver entre colchetes, `[ASSIM]`, sai em vermelho para o analista
completar, e o painel lista essas lacunas antes de gerar.

- O rascunho fica dentro do caso, em `<caso>\iped-pcba-relatorio\rt.json`, com cada versão anterior
  em `historico\`. O `.docx` sai em `<caso>\iped-pcba-relatorio\RT.docx`.
- Os dados da unidade (cabeçalho, endereço, sigla, núcleo, e-mails que entram em todo pedido e
  analistas padrão) são preenchidos uma vez no painel e ficam em `~\.iped-pcba\unidade.json`.
  Nada da unidade está fixo no código: cada delegacia preenche os seus.
- "Calcular SHA-256" faz o hash da `Lista de Arquivos.csv` exportada do IPED e o põe na metodologia.
- A IA pode escrever o rascunho pelo MCP (`get_report_draft`, `update_report_field`,
  `update_report_analysis`). Tudo o que ela escreve aparece no painel como "Escrito pela IA:
  revise". A conclusão de cada análise começa como lacuna: quem conclui é o analista.
- O `.docx` é gerado só com a biblioteca padrão do Python, então funciona com o Python que já vem
  no IPED, sem instalar nada.

Pelo console: `python -m iped_pcba relatorio gerar --caso <pasta>` (também `lacunas` e `telematica`).

### Registros telemáticos padronizados

Todo retorno de provedor vira o mesmo CSV (separador `;` ou `,`), um registro por linha:

| Coluna | Conteúdo |
|---|---|
| `provedor` | WhatsApp, Google, Apple, Meta, operadora… |
| `conta` | conta investigada (telefone, e-mail, ID) |
| `tipo` | `mensagem`, `chamada`, `conexao`, `login`, `localizacao`, `contato`, `grupo` ou `outro` |
| `data_hora` | ISO 8601 com fuso (`2026-03-01T13:05:00Z`); sem fuso é tratado como UTC |
| `interlocutor`, `direcao` | outra ponta da mensagem ou chamada, `enviada`/`recebida` |
| `ip`, `porta` | IP e porta lógica do registro de conexão |
| `dispositivo`, `grupo`, `duracao_s`, `local`, `fonte` | quando o provedor informa; `fonte` é o arquivo de origem |

"Importar e resumir" no passo 5 lê esse CSV e cria, por provedor, a tabela de contas, um texto de
rascunho em prosa (período em horário de Brasília, volume por tipo, principais interlocutores, IPs
mais recorrentes com portas, dispositivos, grupos e faixa horária) e os quadros de interlocutores e
de IPs. Análises que o analista já editou não são substituídas numa nova importação. Os conversores
de cada provedor para esse CSV são a fase 3. Exemplo com dados fictícios:
`tests/fixtures/telematica/registros_ficticios.csv`.

## Autorização de uso

O Vestígio só funciona nas máquinas que eu autorizo, e cada versão nova precisa de uma renovação.

1. Na primeira vez, o painel abre só a tela **Autorização de uso**: o analista preenche nome, instituição e contato e clica em **Gerar pedido**. Sai um código `VPED-…` com esses dados, a versão e uma identificação da máquina (um resumo que não revela nada dela). Ele me envia o código como preferir (e-mail, mensagem, ofício).
2. Eu colo o pedido na tela **Autorizações** do meu painel (ela só aparece na máquina que tem a chave privada) e devolvo um código `VAUT-…`, assinado com Ed25519. Posso dar validade em dias e liberar a série toda (ex.: 0.6.1, 0.6.2) em vez de só a versão pedida.
3. O analista cola o código, clica em **Ativar** e o painel libera.
4. Quando sai uma versão nova, o painel continua funcionando na atual, baixa a nova e mostra **Gerar pedido de renovação**. A nova só é instalada depois que a renovação é ativada.

A chave pública fica em `instalador/iped_pcba/autorizacao.json`; a privada fica só na minha máquina, em `~/.iped-pcba/autorizacao-emissor/chave-privada.txt`. Outra instituição que use o Vestígio pode gerar a própria chave com `python -m iped_pcba.autorizacao gerar-chave` e trocar a pública no `autorizacao.json`. Sem chave pública, ou numa cópia de desenvolvimento (git), nada é exigido.

**O que isto não impede:** o código é Python legível, então quem tem o pacote consegue alterar o programa para pular a verificação, e uma cópia antiga continua funcionando na versão para a qual foi autorizada. É um controle de quem recebe e atualiza o Vestígio, não uma trava contra quem quer burlar.

## O que a configuração faz

Nessa ordem:

1. **Acha o IPED**: primeiro o caminho que o próprio IPED registra em `~\.iped\ipedRoot.txt`,
   depois a variável `IPED_ROOT`, depois procura em todos os discos (raiz, `Tools`,
   `Program Files`, Área de Trabalho, Downloads, Documentos) até três níveis. Se houver mais de
   uma instalação, usa a de versão mais nova e lista as outras.
2. **Reconhece a máquina**: CPU, RAM, discos e espaço livre, SSD ou HDD, GPU NVIDIA com VRAM,
   driver e CUDA, versão do IPED e pacotes de IA no Python do IPED.
3. **Escolhe a pasta temporária**: o SSD fora do disco do sistema com mais espaço livre (mínimo
   50 GB); se não houver, o SSD do sistema; se não houver SSD, o disco com mais espaço.
4. **Monta o plano**, com o motivo de cada mudança:
   - `LocalConfig.txt`: `locale = pt-BR`, `indexTemp`, `indexTempOnSSD` só em SSD,
     `outputOnSSD`, `numThreads` limitado quando a RAM é curta;
   - `conf/HashTaskConfig.txt`: inclui SHA-256 (anexos do WhatsApp e cadeia de custódia);
   - `conf/AudioTranscriptConfig.txt`: Whisper em GPU com o modelo
     `deepdml/faster-whisper-large-v3-turbo-ct2` (large-v3-turbo, a partir de 6 GB de VRAM),
     Whisper em CPU, transcrição no servidor central ou Vosk. Nunca liga o Whisper se o
     `faster-whisper` não estiver no Python do IPED, para não quebrar o processamento;
   - heap da JVM: 50% da RAM com teto de 30 GB.
5. **Mostra o plano** e só grava quando você manda, com backup em `<IPED>\pcba\backup\<data-hora>\`.
6. **Gera os perfis** `pcba-celular`, `pcba-computador`, `pcba-telematica` e `pcba-triagem`.
7. **Gera o lançador** `<IPED>\pcba\iped-pcba.bat` e grava `<IPED>\pcba\maquina.json` com o
   retrato da máquina e o que mudou.
8. **Instala o MCP** (IA) em `<IPED>\pcba\mcp\`, com o lançador `iped-pcba-mcp.bat` e o trecho
   de configuração para o Claude Desktop e o LM Studio. Com escrita liberada (a IA cria
   marcadores e comentários; desligue no painel ou com `--somente-leitura`) e com log de
   auditoria no próprio caso. Detalhes no `mcp/README.md` que vai no pacote.
9. **Instala o painel** em `<IPED>\pcba\app\` e o lançador `<IPED>\pcba\painel-pcba.bat`.

Opções do `scripts\instalar.ps1` (o `instalar.bat` repassa todas):

| Opção | Efeito |
|---|---|
| `-IpedRoot <pasta>` | usa esta instalação em vez de procurar |
| `-Temp <pasta>` | usa esta pasta temporária em vez de escolher |
| `-ServidorTranscricao IP:PORTA` | manda a transcrição para o servidor central |
| `-Texto` | configuração pelo console, sem o painel |
| `-Simular` | mostra o que mudaria, sem gravar |
| `-Aplicar` | aplica sem perguntar (implantação em lote, GPO) |
| `-Reverter` | desfaz a última aplicação (inclusive o MCP) |

Se o IPED estiver em `Program Files`, rode como administrador.

Depois de aplicado, para processar:

```bat
<pasta do IPED>\pcba\iped-pcba.bat pcba-celular <evidência> <pasta do caso>
```

## Instalar no servidor Linux central

```bash
bash scripts/instalar.sh baixar /opt/iped                   # só se ainda não houver IPED
bash scripts/instalar.sh <pasta do IPED> diagnosticar --papel servidor
bash scripts/instalar.sh <pasta do IPED> aplicar      --papel servidor
<pasta do IPED>/pcba/transcricao-servidor.sh 11111 11112   # descoberta + serviço de transcrição
```

As estações passam a usar o servidor com `instalar.bat -ServidorTranscricao IP-do-servidor:11111`.

### Whisper em GPU

- Windows: `scripts\\whisper_gpu.ps1 -IpedRoot <pasta do IPED>` (simula por padrão; `-Execute` aplica).
  Pré-requisitos manuais: Visual C++ Redistributable x64 e driver NVIDIA com CUDA 12.
- Linux: `pip install faster-whisper` no Python usado pelo IPED, com CUDA 12 e cuDNN do sistema.

Depois de instalar, rode o instalador de novo: ele passa a detectar o `faster-whisper` e liga o
Whisper.

Em GPU o modelo recomendado é o `deepdml/faster-whisper-large-v3-turbo-ct2` (large-v3-turbo
convertido para o faster-whisper): transcreve melhor que o `medium` e é mais rápido que o
`large-v3`. Em CPU fica o `small`, porque o turbo seria lento demais para o volume de áudios. O
faster-whisper baixa o modelo do Hugging Face (cerca de 1,6 GB) na primeira transcrição, então
essa primeira vez precisa de internet; depois ele fica no cache do usuário
(`%USERPROFILE%\.cache\huggingface`). Em máquina sem internet, copie essa pasta de cache de outra
estação ou aponte `whisperModel` para uma pasta local com o modelo.

### Confirmação da GPU durante o processamento

No IPED 4.3 quem usa a placa NVIDIA é a transcrição de áudio. Em máquina com NVIDIA, o painel roda o
IPED com `-log` e lê nesse log em que dispositivo o modelo de transcrição carregou
(`Model loaded on device=cuda`). No progresso aparece **GPU ativada** quando o IPED confirma. Quando
não ativa, aparece o alerta com o motivo (transcrição configurada para o processador, Vosk ou outro
serviço, falta do faster-whisper ou do GPUtil no Python do IPED, CUDA não instalado e DLLs dele fora
da pasta `python` do IPED, com o nome de cada DLL que falta, placa NVIDIA sem driver, driver que não
chega ao CUDA 12, falta de memória na placa) e a pergunta **Deseja corrigir e recomeçar?**:

- **Corrigir e recomeçar** para o IPED, liga a GPU no `AudioTranscriptConfig.txt` do perfil (com
  backup em `pcba\backup`) ou instala o CUDA no Python do IPED (`whisper_gpu.ps1`, precisa de
  internet) e processa o caso de novo do zero (`--restart`). Na fila, o caso recomeçado continua no
  mesmo lugar.
- **Continuar sem GPU** segue o processamento no processador.

Em máquina sem NVIDIA, ou com perfil que não transcreve áudio, nada aparece.

## Perfis

| Perfil | Base | Para quê |
|---|---|---|
| `pcba-celular` | raiz | Extrações de celular. Transcrição, grafo, QR code, similaridade de imagens. |
| `pcba-computador` | forensic | Imagens de disco. Carving, transcrição, grafo. |
| `pcba-telematica` | raiz | Retornos de provedores. Expande pacotes, indexa conteúdo e regex, sem carving. |
| `pcba-triagem` | triage | Triagem em local de busca, sem transcrição. |

A tela Processar evidência explica cada perfil (quando usar, o que liga e desliga, tempo) e os
perfis do próprio IPED (`forensic`, `pedo`, `fastmode`, `triage`, `blind`).

O IPED aplica a raiz e depois o perfil: o `IPEDConfig.txt` do perfil substitui o da raiz e cada
arquivo em `profiles/<perfil>/conf/` substitui o de mesmo nome em `conf/`. Por isso os perfis são
gerados como cópia completa da base com as chaves da PCBA por cima, e o que depende da máquina
(transcrição, hashes, temp) fica na raiz, valendo para todos os perfis.

## Regras do projeto

- Nenhum dado real de investigação entra neste repositório, em testes ou em prompts.
- IA local por padrão; Claude Desktop e Hermes Agent são opções do analista, não do instalador.
- Toda conclusão de IA passa por revisão humana antes de ir para um relatório.

## Próximas fases

3. Conversores dos retornos de provedores (WhatsApp, Google, Apple, Meta) para o CSV padronizado e
   importador do Guardião (Dígitro). Dependem de amostras anonimizadas.

## Desenvolvedor

Desenvolvido por Marcus ([@marcusvlessa](https://github.com/marcusvlessa)).
[Saiba mais sobre o desenvolvedor](https://www.linkedin.com/in/marcuslessa-ia/).

## Licença

GPLv3, a mesma do IPED. O código-fonte vai dentro de cada pacote.
