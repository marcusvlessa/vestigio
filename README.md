<div align="center">
  <img src="docs/media/logo-lite.png" alt="Vestígio LITE" width="96" />
  <h1>Vestígio LITE</h1>
  <p><em>Versão LITE de um projeto em parceria com a Universidade Federal da Bahia (UFBA), parte de um estudo de doutorado em Ciência da Computação (PGCOMP).</em></p>
  <p><strong>Assistente de análise forense para o IPED: instala, configura, analisa com IA local auditada e entrega o relatório no modelo da sua instituição.</strong></p>
  <p>
    <a href="https://github.com/marcusvlessa/vestigio/releases/latest">Baixar</a> ·
    <a href="#instalar">Instalar</a> ·
    <a href="#o-que-ele-faz">O que ele faz</a> ·
    <a href="#versão-lite-e-a-pesquisa">Versão LITE</a> ·
    <a href="#autorização-de-uso">Autorização de uso</a> ·
    <a href="#desenvolvedor">Desenvolvedor</a> ·
    <a href="https://github.com/sponsors/marcusvlessa">Apoiar</a>
  </p>
  <p>
    <a href="https://github.com/marcusvlessa/vestigio/releases/latest"><img src="https://img.shields.io/github/v/release/marcusvlessa/vestigio?label=vers%C3%A3o" alt="Versão mais nova" /></a>
    <a href="https://github.com/marcusvlessa/vestigio/releases"><img src="https://img.shields.io/github/downloads/marcusvlessa/vestigio/total?label=downloads" alt="Downloads" /></a>
    <img src="https://img.shields.io/badge/vers%C3%A3o-LITE-1f9e94" alt="Versão LITE" />
    <img src="https://img.shields.io/badge/pesquisa-UFBA%20%C2%B7%20PGCOMP-0d2f57" alt="Pesquisa UFBA PGCOMP" />
    <img src="https://img.shields.io/badge/Windows%20%7C%20Linux-0d2f57" alt="Windows e Linux" />
    <img src="https://img.shields.io/badge/IPED-4.3.1-c9a227" alt="IPED 4.3.1" />
    <img src="https://img.shields.io/badge/licen%C3%A7a-GPLv3-blue" alt="GPLv3" />
    <a href="https://github.com/sponsors/marcusvlessa"><img src="https://img.shields.io/github/sponsors/marcusvlessa?label=apoiar&logo=githubsponsors&color=ea4aaa" alt="Apoiar no GitHub Sponsors" /></a>
  </p>
</div>

![Um passeio pelo painel: visão do caso, rede de vínculos, análise financeira, assistente de IA e relatório técnico](docs/media/vestigio.gif)

<p align="center"><sub>Todos os dados das telas são fictícios.</sub></p>

## Versão LITE e a pesquisa

Esta é a **versão LITE** do Vestígio: a linha de base pública de um projeto desenvolvido em parceria
com a **Universidade Federal da Bahia (UFBA)**, como parte de um estudo de doutorado em Ciência da
Computação (PGCOMP). Ela funciona por completo e é a referência com que a pesquisa compara os
resultados. A versão completa, em desenvolvimento no doutorado, será avaliada em pilotos nas delegacias.

| | **LITE (esta página)** | **Versão completa (em pesquisa)** |
| :--- | :--- | :--- |
| Papel no estudo | linha de base: o trabalho de hoje com o painel e a IA local | intervenção avaliada nos pilotos |
| IA | consulta o caso pelo MCP, com auditoria; qualidade ainda não medida | IA medida (acurácia, alucinação, tempo) em casos sintéticos |
| Afirmações da IA | o analista confere | cada afirmação verificada contra o item do IPED que a sustenta |
| Instruções escondidas no material apreendido | aviso ao analista | defesa automática contra injeção pela evidência |
| Proveniência | registro encadeado por hash, local | proveniência forte, ancorada fora da máquina |

Novidades desta versão LITE: o passo **Configurar a máquina** instala tudo o que falta, incluindo o
CUDA da placa NVIDIA para o Whisper; as janelas de **Procurar** abrem sempre por cima; e o
**Assistente de IA** coloca o caminho do caso e da pasta de contexto na pergunta copiada para o
Claude, o Antigravity ou o Hermes.

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

## O que ele faz

O Vestígio é um painel que acompanha o analista do começo ao fim de um caso no [IPED](https://github.com/sepinf-inc/IPED). Serve a qualquer instituição de segurança: polícias, perícias, núcleos de inteligência e Ministério Público.

- **Instala e configura o IPED sozinho.** Descobre o que a máquina tem e instala o que falta (IPED, transcrição de áudio, reconhecimento facial, IA local). Guarda uma cópia da configuração antes de mudar qualquer coisa.
- **Processa as evidências em fila**, com o progresso na tela, e escolhe o perfil certo para celular, computador ou retorno de provedor.
- **Mostra o caso de forma visual:** visão geral com alertas, rede de vínculos, linha do tempo, mapa de localizações e registros telemáticos.
- **Faz a análise financeira** de SIMBA, RIF e extratos, com alertas e um painel que funciona sem internet.
- **Traz um assistente de IA local** que consulta o caso, descreve imagens e vídeos e refaz transcrições de baixa qualidade. Cada consulta fica registrada no log de auditoria do caso.
- **Gera o relatório** no modelo da sua instituição, em .docx.

Os dados do caso ficam na sua máquina. A IA local é o padrão. Ligar uma IA na nuvem é opcional, e o painel avisa antes.

## Instalar

1. Baixe o pacote da [versão mais nova](https://github.com/marcusvlessa/vestigio/releases/latest):
   - **Windows:** `iped-pcba-windows.zip`. Descompacte em qualquer pasta e dê dois cliques em `Vestigio.exe`.
   - **Linux (servidor):** `iped-pcba-linux.tar.gz`. Descompacte e rode `scripts/instalar.sh`.
2. Na primeira vez, peça a autorização de uso (veja abaixo).
3. Siga os passos do painel. Ele mostra o que falta na máquina e instala com um clique.

Não é preciso instalar Python nem o IPED antes. Se a máquina não tiver o IPED, o Vestígio oferece baixar a versão oficial.

## Autorização de uso

O Vestígio só funciona em máquinas autorizadas, e cada versão nova precisa de uma renovação.

1. Na primeira vez, o painel abre na tela **Autorização de uso**. Preencha nome, instituição e contato e clique em **Gerar pedido**.
2. Envie o código do pedido ao [desenvolvedor](#desenvolvedor).
3. Cole o código de autorização que receber e clique em **Ativar**.

Quando sai uma versão nova, o painel continua funcionando na atual e mostra **Gerar pedido de renovação**. A nova versão é instalada depois que a renovação é ativada.

**Uso da pesquisa.** Como parte do estudo de doutorado, o painel envia sozinho ao desenvolvedor, ao abrir e a cada hora de uso, um resumo de uso desta máquina: nome, instituição, identificação da máquina, versão, total de aberturas, datas de primeiro e último uso e sistema. Nunca sai dado de caso ou evidência. O próprio painel mostra, na tela inicial, o que é enviado.

## Atualizações

O painel procura versões novas sozinho e baixa em segundo plano. A versão anterior fica guardada numa pasta ao lado, caso seja preciso voltar.

## Desenvolvedor

Marcus ([@marcusvlessa](https://github.com/marcusvlessa)) · [Saiba mais sobre o desenvolvedor](https://www.linkedin.com/in/marcuslessa-ia/)

## Apoie o projeto

Se o Vestígio ajuda no seu trabalho, você pode apoiar pelo [GitHub Sponsors](https://github.com/sponsors/marcusvlessa) para manter o projeto atualizado e funcionando.

## Licença

GPLv3, a mesma do IPED.
