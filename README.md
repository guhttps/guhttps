<h1 align="center">GUH.</h1>

<picture>
  <source media="(prefers-reduced-motion: no-preference)" srcset="https://raw.githubusercontent.com/guhttps/guhttps/main/assets/edward-elric.gif" type="image/gif" />
  <img align="right" src="https://raw.githubusercontent.com/guhttps/guhttps/main/assets/edward-elric.jpg" width="210" alt="Edward Elric" />
</picture>

<p>
  <strong>Meus projetos nascem da vontade de ajudar.</strong><br />
  Estudante de <strong>Engenharia de Software</strong>.<br />
  Gosto de criar soluções que simplificam as coisas e facilitam o dia a dia.
</p>

<p>
  <a href="#meu-laboratório">Tecnologias</a> &nbsp;·&nbsp;
  <a href="#projetos-em-transmutação">Projetos</a> &nbsp;·&nbsp;
  <a href="#meu-setup">Meu setup</a> &nbsp;·&nbsp;
  <a href="#certificados">Certificados</a>
</p>

<br clear="both" />

## Meu laboratório

<picture>
  <source media="(prefers-reduced-motion: no-preference)" srcset="https://raw.githubusercontent.com/guhttps/guhttps/main/assets/alphonse-elric.gif" type="image/gif" />
  <img align="left" src="https://raw.githubusercontent.com/guhttps/guhttps/main/assets/alphonse-elric.jpg" width="170" alt="Alphonse Elric" />
</picture>

<p>
  <img src="https://raw.githubusercontent.com/guhttps/guhttps/main/assets/python.svg" height="30" alt="Python" />
  <img src="https://raw.githubusercontent.com/guhttps/guhttps/main/assets/powershell.svg" height="30" alt="PowerShell" />
  <img src="https://raw.githubusercontent.com/guhttps/guhttps/main/assets/git.svg" height="30" alt="Git" />
</p>

<br clear="both" />

## Projetos em transmutação

| Projeto | O que você encontra |
| :--- | :--- |
| 🖥️ **[Multiseat Windows](https://github.com/guhttps/multiseat-windows)** | Painel experimental para planejar duas estações no Windows, com instalador e ZIP disponíveis. Motor multiseat em pesquisa. |
| 🎙️ **[LoL AI Coach](https://github.com/guhttps/lol-ai-coach)** | Coach de League of Legends com IA, interação por voz e overlay. Feito em Python. |
| ⚙️ **[BO2 + Plutonium](https://github.com/guhttps/bo2-plutonium-instalador)** | Assistente para Windows com download retomável e verificação de integridade. Feito em PowerShell. |

### Multiseat Windows · projeto público

[![Compilação Windows](https://github.com/guhttps/multiseat-windows/actions/workflows/windows-build.yml/badge.svg?branch=main)](https://github.com/guhttps/multiseat-windows/actions/workflows/windows-build.yml)
[![Verificações de privacidade](https://github.com/guhttps/multiseat-windows/actions/workflows/security.yml/badge.svg?branch=main)](https://github.com/guhttps/multiseat-windows/actions/workflows/security.yml)
[![Análise de segurança C++ e C#](https://github.com/guhttps/multiseat-windows/actions/workflows/codeql.yml/badge.svg?branch=main)](https://github.com/guhttps/multiseat-windows/actions/workflows/codeql.yml)

O objetivo é criar estações independentes no mesmo computador Windows, cada uma com sua conta, monitor, teclado e mouse. O código e a documentação já são públicos.

[Ver o projeto](https://github.com/guhttps/multiseat-windows) · [Código e documentação](https://github.com/guhttps/multiseat-windows/blob/main/README.md) · [Acompanhar o desenvolvimento](https://github.com/guhttps/multiseat-windows/issues)

**Painel experimental disponível:** [baixar instalador Windows x64](https://github.com/guhttps/multiseat-windows/releases/download/v0.1.0-experimental.1/MultiseatPrototype-0.1.0-experimental.1-windows-x64-installer.exe) · [ZIP portátil e notas da versão](https://github.com/guhttps/multiseat-windows/releases/tag/v0.1.0-experimental.1) · [como instalar e usar](https://github.com/guhttps/multiseat-windows/blob/main/docs/DOWNLOAD-INSTALL.md). A instalação é por usuário, sem administrador. A versão é experimental, sem assinatura de código, e ainda não ativa estações independentes para jogos ou aplicativos externos.

**Pesquisa atual (21/10/2026):** o laboratório separado em Windows Server/RDS validou duas contas em aplicativos externos, reabertura física por F7 nos dois sentidos e quatro cenários automáticos de remoção/reassociação simulada pelo roteador de produção; uma observação anterior reuniu 130 amostras em 30 minutos. [Resultados e limites do laboratório](https://github.com/guhttps/multiseat-windows/blob/84b9d1f1e6edd1235806c662f462af24ca7eaa7a/docs/lab/008-rds-transport-comparison.md). O núcleo nativo começou com captura de identidade a partir de token primário real e reservas não interativas de recursos, com revisão independente e 15 verificações locais aprovadas na configuração completa. Os testes cobrem retiradas de dispositivos desconhecidos ou de geração mais nova e falhas de alocação. [Base nativa e limites](https://github.com/guhttps/multiseat-windows/blob/ab0a05a857b01a832c2d922effad1b080016b77e/docs/architecture/0009-native-core-and-session-research.md). O terminal nativo utilizável, a apresentação e entrada independentes, áudio e LoL permanecem pendentes. O ciclo físico completo com cabos também continua pendente.

**Laboratório do motor nativo:** a VM Windows cliente já tem checkpoint limpo e recuperação externa verificada em três cenários: prazo esgotado, perda do coordenador e tarefa benigna sem resposta. [Resultados e limites](https://github.com/guhttps/multiseat-windows/blob/4be9d2363b126c7856505923d50c581c17d2320d/docs/lab/009-native-h1-recovery.md). Essa etapa prepara a pesquisa; ainda não cria o segundo terminal nativo.

**Criação nativa de sessão:** uma solicitação limitada na VM cliente criou outra sessão com CSRSS e o processo inicial de teste, preservou o console original e terminou com restauração externa verificada. [Prova e limites](https://github.com/guhttps/multiseat-windows/blob/17e6000b5d0cdf27f5887e938b6521022a54adc5/docs/lab/010-native-session-creation.md). Esse resultado ainda não fornece login de uma segunda conta nem um posto com tela e entrada próprias.

**Integração do terminal nativo:** o serviço real validou o cliente do ensaio, consultou `IWRdsWddmIddProps1` e completou `OnConnected`, `OnReady`, recusa controlada em `AcceptConnection` e `Close`, com restauração externa conferida. A sequência usou uma exceção experimental de uso único, restrita à imagem validada da VM; ainda não comprova conexão aceita nem segundo terminal utilizável. A próxima integração trata dos canais reais de entrada e da ligação entre sessão e display. A base inclui leitura de texturas D3D11 e protocolo de status com 223 verificações em memória. O pacote privado foi assinado e aceito no DriverStore da VM, mas requisição WDF, driver carregado, frames de desktop e saída física continuam pendentes. [Admissão e limites](https://github.com/guhttps/multiseat-windows/blob/14f5630c2b3422fff046dd3d756b91fe11449c59/docs/lab/014-native-local-admission.md) · [protocolo e limites](https://github.com/guhttps/multiseat-windows/blob/14f5630c2b3422fff046dd3d756b91fe11449c59/docs/lab/016-native-driver-channel.md) · [mudança revisada](https://github.com/guhttps/multiseat-windows/pull/41) · [entregas pendentes](https://github.com/guhttps/multiseat-windows/blob/14f5630c2b3422fff046dd3d756b91fe11449c59/docs/REMAINING-WORK.md).

<picture>
  <source media="(prefers-reduced-motion: no-preference)" srcset="https://raw.githubusercontent.com/guhttps/guhttps/main/assets/sung-jinwoo.gif" type="image/gif" />
  <img align="right" src="https://raw.githubusercontent.com/guhttps/guhttps/main/assets/sung-jinwoo.jpg" width="150" alt="Sung Jinwoo" />
</picture>

<p>
  <a href="https://github.com/guhttps?tab=repositories">Explorar meus repositórios →</a>
</p>

<br clear="both" />

## Meu setup

<picture>
  <source media="(prefers-reduced-motion: no-preference)" srcset="https://raw.githubusercontent.com/guhttps/guhttps/main/assets/arthur-leywin.gif" type="image/gif" />
  <img align="left" src="https://raw.githubusercontent.com/guhttps/guhttps/main/assets/arthur-leywin.jpg" width="110" alt="Arthur Leywin" />
</picture>

| Componente | Hardware |
| :--- | :--- |
| Processador | AMD Ryzen 9 7900 |
| Placa de vídeo | NVIDIA GeForce RTX 4060 |
| Memória RAM | 32 GB DDR5 · 2 × 16 GB · 5200 MT/s |
| Placa-mãe | ASUS TUF GAMING B650M-PLUS |
| SSD 1 | XPG GAMMIX S70 BLADE · 1 TB |
| SSD 2 | ADATA NVMe · 512 GB |

<br clear="both" />

## Certificados

| Curso | Instituição | Carga horária | Certificado |
| :--- | :--- | :---: | :--- |
| Linguagem de Programação Python — Básico | Fundação Bradesco · Escola Virtual | 18 horas | [Ver PDF](certificados/python.pdf) |
| Fundamentos de TI: Hardware e Software | Fundação Bradesco · Escola Virtual | 7 horas | [Ver PDF](certificados/fundamentos-ti-hardware-software.pdf) |

<p align="center">
  <sub>A próxima transmutação começa com uma ideia.</sub>
</p>
