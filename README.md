<h1 align="center">Ygor A. Silman</h1>

<p align="center">
  <b>Segurança da Informação · FIAP</b> · Automação de processos (RPA) em Python
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python" />
  <img src="https://img.shields.io/badge/Selenium-43B02A?style=for-the-badge&logo=selenium&logoColor=white" alt="Selenium" />
  <img src="https://img.shields.io/badge/Kali_Linux-557C94?style=for-the-badge&logo=kalilinux&logoColor=white" alt="Kali Linux" />
  <img src="https://img.shields.io/badge/Arch_Linux-1793D1?style=for-the-badge&logo=archlinux&logoColor=white" alt="Arch Linux" />
  <img src="https://img.shields.io/badge/Bash-4EAA25?style=for-the-badge&logo=gnubash&logoColor=white" alt="Bash" />
  <img src="https://img.shields.io/badge/WireGuard-88171A?style=for-the-badge&logo=wireguard&logoColor=white" alt="WireGuard" />
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="JavaScript" />
  <img src="https://img.shields.io/badge/SQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white" alt="SQL" />
  <img src="https://img.shields.io/badge/Claude-D97757?style=for-the-badge&logo=anthropic&logoColor=white" alt="Claude" />
</p>

---

## 🚀 Sobre

Trabalho como escrevente num Cartório de Registro Civil em São Paulo: certidões,
inteiros teores, controle de pedidos, atendimento no balcão. Foi ali que comecei a
automatizar. Cada robô deste perfil nasceu de uma tarefa que eu fazia à mão, todo
dia, e que dava pra conferir por regra: a declaração de selos preenchida lendo PDF
linha por linha, as anotações digitadas no sistema uma por uma, as etiquetas dos
Correios montadas na mão.

Em paralelo, curso **Segurança da Informação na FIAP**. As duas coisas se
encontram mais do que parece. O cartório lida com documento que vale como prova e
com dado pessoal sob LGPD, e um robô que gera documento pra alguém assinar precisa
pensar como auditor: **documento errado é pior que documento faltando.**

Inglês avançado. Uso Linux (Arch + Hyprland) no dia a dia e IA como ferramenta de
trabalho, sem deixar de ler o que vai pro código.

---

## 🛡️ Segurança

Trilha da FIAP, com o que foi pra prática:

| | |
|---|---|
| 🔍 **Testes éticos — Challenge FIAP + CEAP** | Em grupo, testes controlados no ambiente de homologação de uma escola técnica parceira: reconhecimento, análise e exploração controlada, PoC e mitigações, entregues em relatório final |
| 🚩 **CTF Wargames** | Global Solution em formato CTF, com write-up técnico de cada desafio do início ao fim |
| 🧪 **Correção de XSS** | No projeto *Gasto na Foto* (evento DevClub), reescrevi a versão final trocando `innerHTML` por `textContent`/`createElement`, validando entrada e tirando handler inline |
| 🌐 **VPN própria** | Servidor WireGuard em casa com DDNS por timer do systemd, firewall (`ufw`) restrito à interface da VPN e testado de fora da rede pelo 5G |

**Conteúdo estudado:** OSINT e OpSec · resposta a incidentes · Active Directory ·
ataques ofensivos · análise de malware e engenharia reversa · segurança em nuvem
(AWS) e de IA/LLM · governança, LGPD, ITIL e gestão de riscos · forense digital ·
pentest mobile.

---

## 💼 Projetos

### 🏷️ [Robô de Selos por Guichê](https://github.com/Alphabittest/robo-selos)
**Em uso em produção no cartório.** Lê o relatório diário de selos (PDF), confere os
números e gera a declaração de cada guichê pronta pra assinar.

As regras de negócio não estavam escritas em lugar nenhum: descobri lendo os
relatórios e validei contra **68 declarações preenchidas à mão**. São 4 conferências
antes de gerar qualquer coisa. Se uma falha, **nenhuma** declaração sai, porque
ninguém pode assinar por um selo que não usou. Só biblioteca padrão do Python: o
`.docx` é aberto como zip e preenchido direto no XML.

<img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" /> <img src="https://img.shields.io/badge/Tkinter-3776AB?style=flat-square" /> <img src="https://img.shields.io/badge/pdftotext-555555?style=flat-square" /> <img src="https://img.shields.io/badge/unittest-555555?style=flat-square" />

### 🤖 Robôs de rotina do cartório
**Quatro etapas do fluxo que eram manuais.** Anotação automática de nascimento e
casamento no sistema; rejeição de comunicados duplicados na central do Registro
Civil (o login é feito por uma pessoa e o robô continua sozinho); endereçador dos
Correios que lê o PDF do pedido e imprime as etiquetas; e uma fila para comunicados
internos (divórcio, casamento, óbito) que extrai vara, foro e autos por regex.

<sub>Código de uso interno, com dados reais: não é público.</sub>

<img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" /> <img src="https://img.shields.io/badge/Selenium-43B02A?style=flat-square&logo=selenium&logoColor=white" /> <img src="https://img.shields.io/badge/PyAutoGUI-555555?style=flat-square" /> <img src="https://img.shields.io/badge/pdfplumber-555555?style=flat-square" />

### 📝 Ficha cadastral online para imobiliária
**Proposta de compra sem papel.** A corretora gera o link e manda no WhatsApp com os
dados do cliente já preenchidos; o cliente preenche até 4 compradores, anexa os
documentos (comprimidos no próprio celular) e tudo chega por e-mail. Montada e
entregue para uso real. Os documentos não passam por mim: cada imobiliária roda
na própria conta (LGPD).

<img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black" /> <img src="https://img.shields.io/badge/Google_Apps_Script-4285F4?style=flat-square&logo=google&logoColor=white" /> <img src="https://img.shields.io/badge/Netlify-00C7B7?style=flat-square&logo=netlify&logoColor=white" />

### 🐧 Dual boot Arch Linux + Hyprland
**Liberei 115 GB num SSD em que o Windows não deixava encolher a partição.** O
`shrink` travava em arquivos imóveis no fim do volume. Em vez de chutar, achei o
culpado de cada vez pelo evento 259 do log do Windows (`swapfile.sys`, `pagefile.sys`
e o USN Journal), resolvi um por reboot e confirmei cada medição duas vezes.

<img src="https://img.shields.io/badge/Arch_Linux-1793D1?style=flat-square&logo=archlinux&logoColor=white" /> <img src="https://img.shields.io/badge/Hyprland-58E1FF?style=flat-square" /> <img src="https://img.shields.io/badge/Windows-0078D4?style=flat-square&logo=windows&logoColor=white" />

---

<p align="center">
  <sub>Todo projeto aqui é algo que eu uso ou usei de verdade.</sub>
</p>
