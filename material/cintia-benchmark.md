# Benchmark — URAs e bots de WhatsApp B2B

> Pesquisa de setembro/2026 pra informar o fluxo da CintIA.
> Fontes no fim. O que interessa aqui é **o que a gente aplica**, não o resumo.

---

## 1. O achado que mais importa

**Nenhum concorrente direto cota por WhatsApp.**

| Player | O que é | O WhatsApp deles é |
|---|---|---|
| **Cotefácil** | 17 anos, se posiciona como a líder B2B de cotação farma | canal de suporte e venda |
| **SmartPed** | 300+ distribuidoras integradas, 7.000 farmácias ativas | consultor humano explicando plano |
| **Botfarmax** | automação de atendimento **pra** farmácia (B2C, balcão) | outro problema, não é cotação B2B |

Os dois grandes têm plataforma robusta e WhatsApp só como porta de entrada pra um humano. **Ninguém entrega a cotação dentro da conversa.**

Isso significa duas coisas:

1. A CintIA não é "mais um bot". É a primeira a colocar o produto inteiro dentro do WhatsApp nesse mercado.
2. **Não dá pra copiar de ninguém no setor.** O benchmark útil vem de fora: conversational commerce B2B LatAm (Yalo) e padrões gerais de UX de chatbot.

⚠️ **Régua de mercado pra ter na cabeça:** SmartPed diz 7.000 farmácias ativas e 300+ distribuidoras. É o tamanho do jogo em que a gente está entrando.

---

### 1.1 · Como usar esse diferencial (e como NÃO usar)

⛔ **Antes de tudo: nunca dizer "somos os únicos".**

Três motivos, e o terceiro é o que importa:

1. É uma alegação de superioridade que alguém pode contestar amanhã. Basta um concorrente lançar e a frase vira mentira no ar
2. A pesquisa cobre quem se anuncia na web. Pode existir um piloto que a gente não viu
3. **Bate na regra 5 da spec.** Afirmar o que o concorrente não faz é falar do concorrente. A CintIA não faz isso, e a marca em volta dela também não deveria

✅ **A regra é a mesma da CintIA: afirmar o que a gente FAZ, não o que o outro não faz.** "Cotação completa dentro do WhatsApp" é fato, é diferenciado, e não depende de ninguém. Quem conhece o mercado entende o recado sozinho.

**Onde o diferencial rende:**

| Lugar | O que ele vira | Nota |
|---|---|---|
| **Recado do perfil** (o "sobre" do WhatsApp Business) | *"Manda o remédio que eu te digo onde está mais barato 💊"* | é a primeira coisa que aparece quando salvam o contato |
| **Criativo de anúncio** | o gancho é **a ausência de fricção**: sem portal, sem login, sem senha. Cotar do mesmo lugar onde ela já fala com o representante | ângulo novo pro banco de ganchos |
| **M1 (abertura)** | a promessa já está lá: "me manda o nome e eu te digo o preço em todas as distribuidoras" | ✅ já aplicado |
| **Site / LP** | a seção do WhatsApp deixa de ser "mais um canal de atendimento" e vira produto | combina com a mudança do site que já está na fila |
| **Pitch pro comercial e pra diretoria** | aqui sim vale falar do mercado com todas as letras: nenhum concorrente cota por WhatsApp hoje | é conversa interna, não peça pública |

**O ângulo mais forte pra criativo:** todo mundo do setor já usa WhatsApp o dia inteiro com representante. A novidade não é o canal, é **receber preço de todas as distribuidoras no lugar onde ela já está**, sem abrir mais nada. É disso que o anúncio deveria falar.

---

## 2. Yalo — o padrão do setor lá fora

Yalo é a plataforma de conversational commerce que roda o B2B de Nestlé, Unilever e Coca-Cola FEMSA na América Latina: donos de mercadinho, bar e loja de bairro comprando por WhatsApp.

**O que eles provaram:**

- O pedido inteiro acontece **dentro** do WhatsApp. Não é "clica aqui pra ir pro site". Sair da conversa é onde se perde gente.
- O agente deles (Sales Genie) monta **carrinho já preenchido** com base no histórico de compra, e a pessoa só ajusta.
- Transição de IA pra humano sem quebra é feature de primeira linha, não detalhe.

**O que a gente aplica na v1:** nada de carrinho, mas a direção fica marcada. Hoje a CintIA manda pra plataforma; o caminho natural da v2 é o pedido nascer na conversa. Vale desenhar a v1 sem fechar essa porta.

---

## 3. Os números de UX que valem virar spec

Vindos da literatura de chatbot UX (2026):

| Regra | Número | Por quê |
|---|---|---|
| Tamanho da bolha | **máx. 60 palavras ou 3 frases** | acima disso a pessoa para de ler no celular |
| Uma ideia por bolha | quebrar em limites lógicos | parede de texto mata a conversa |
| Intervalo entre bolhas | **400–700ms** | imita digitação, não parece disparo automático |
| Typing indicator | aparecer em até **200ms**, durar **800ms–1,5s** | sem ele, a pessoa acha que travou |
| Processamento longo | acima de **5s**, mandar status em texto | é exatamente o *"Hmm, deixa eu procurar aqui pra você..."* |
| **Pergunta e botão sempre na ÚLTIMA bolha** | — | pergunta no meio de uma sequência se perde e não é respondida |
| Teste no celular real | 72% das sessões são mobile, e menos de 30% de quem constrói testa no aparelho | testar no aparelho, não no simulador |

✅ **Isso valida a quebra de mensagens que você propôs.** "Oi, eu sou a CintIA" + "qual produto você quer cotar?" em bolhas separadas, com a pergunta por último, é literalmente o padrão recomendado.

---

## 4. Progressive profiling: por que a faixa antes do CNPJ está certa

O consenso da literatura de lead gen conversacional:

> Pedir dado antes de entregar valor afasta. O bot que abre perguntando nome, empresa e e-mail é pior que um formulário, porque finge ser conversa.

E o inverso: pedir **uma coisa de cada vez**, só o necessário naquele momento, e distribuir o resto entre visitas, **reduz abandono**.

**A arquitetura da CintIA já acerta isso:** faixa e quantidade de graça → CNPJ só pra destravar o detalhe → cadastro numa visita futura. O que o benchmark acrescenta é uma regra nova:

⚠️ **Não empilhar dois pedidos na mesma conversa.** Cotação + "se cadastra" + "me salva nos contatos" na primeira visita são três pedidos seguidos. Recomendação aplicada no fluxo: 1ª visita pede só pra salvar o contato; o convite de cadastro entra da 2ª cotação em diante.

---

## 5. ✅ Conflito do falteiro: resolvido (24/09/2026)

O site da [Empresa] promete hoje: que a farmácia manda a foto do falteiro pelo WhatsApp e recebe a lista digitalizada.

**Decisão:** é o mesmo número, e o falteiro por foto **fica fora da v1**. O site vai ser alterado pra tirar a promessa (tarefa da Luiza).

**Enquanto o site não muda**, a CintIA tem resposta própria pra quem chega com foto de falteiro — sem prometer data e sempre oferecendo o caminho que funciona. Texto e regras na seção 9 da spec.

⚠️ **Medir quantas fotos de falteiro chegam.** É a régua da urgência de mudar o site, e o tamanho da demanda real pela feature na v2.

---

## 6. ✅ Duas pendências do FAQ resolvidas pelo próprio site

- **A plataforma é 100% gratuita pra farmácia**, e o site explica quem paga: quem financia a operação é a indústria, o distribuidor e os investidores. Isso destrava a resposta C4 do FAQ, e a explicação de quem paga é o que torna o "é grátis" crível.
- O site promete **condições pelo menos tão boas quanto as do pedido eletrônico que a farmácia já usa**. É a frase que o convite de cadastro pode ecoar, sem inventar promessa nova.

---

## 7. O que NÃO copiar

- **Bot que pergunta "posso ajudar em mais alguma coisa?" no fim.** Pergunta aberta no encerramento exige resposta de quem já foi atendido e gera silêncio constrangido. Melhor uma frase de porta aberta que não pede resposta.
- **Menu numerado de opções na abertura** ("digite 1 para cotar, 2 para falar com atendente"). É a cara de URA de operadora e mata a persona. A CintIA entende texto livre, esse é o ponto dela.
- **Saudação institucional longa.** "A [Empresa] é uma empresa que desde 20XX..." Ninguém lê. O site existe pra isso.

---

## Fontes

- [Yalo — conversational commerce B2B na LatAm (case study)](https://medium.com/@chrishedge/conversational-workflow-builder-yalo-expands-into-native-commerce-to-help-cpgs-better-engage-49ecca1bee14)
- [Yalo (Wikipedia)](https://en.wikipedia.org/wiki/Yalo_(company))
- [Chatbot UX best practices 2026 — BotHero](https://blog.bothero.ai/chatbot-ux-best-practices-the-cognitive-playbook-12-interface-decisions-that-determine-whether-users-trust-your-bot-in-4-seconds-or-close-the-widget-forever)
- [Chatbot UI/UX design best practices — Lollypop](https://lollypop.design/blog/2025/january/chatbot-ui-ux-design-best-practices-examples/)
- [WhatsApp chatbot ultimate guide — BusinessChat](https://www.businesschat.io/post/whatsapp-chatbot-ultimate-guide)
- [Lead qualification chatbot / progressive profiling — Landbot](https://landbot.io/blog/lead-qualification-bot)
- [Como chatbots qualificam leads — Spur](https://www.spurnow.com/en/blogs/how-do-chatbots-qualify-leads)
- [Cotefácil](https://www.cotefacil.com/)
- [SmartPed](https://smartped.net.br/)
- [Site da [Empresa]](https://empresa.example)
