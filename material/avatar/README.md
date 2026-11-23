# Avatar da CintIA — foto de perfil do WhatsApp

> Item da checklist "Perfil do WhatsApp Business" da spec (`../cintia-ura-whatsapp.md`, seção 1):
> *"Foto de perfil: um rosto/avatar reconhecível — não o logo. Contato salvo com logo parece
> empresa; com rosto parece pessoa."*
> Feito em 09/10/2026.

---

## O que tem nesta pasta

| Arquivo | O que é |
|---|---|
| `cintia-A.png` … `cintia-D.png` | as 4 opções, 1024×1024 |
| `cintia-avatar.html` | o gerador. Abre no Chrome com parâmetros na URL e muda pele, cabelo e fundo |
| `teste-corte.html` / `.png` | as 4 opções cortadas em círculo a 200 / 96 / 48px + simulação da lista de conversas |

**As 4 opções**

| | Cabelo | Pele | Fundo |
|---|---|---|---|
| **A** ⭐ | cacheado, volume | morena média | magenta #DC36C0 |
| **B** | longo liso | morena clara | rosa claro #F9C0EA |
| **C** | cacheado, volume | retinta | magenta #DC36C0 |
| **D** | longo liso | morena média | magenta #DC36C0 |

---

## A pesquisa de mercado (o que decidiu o desenho)

### 1. No Brasil, assistente de marca é quase sempre uma mulher ilustrada com nome próprio

Lu (Magalu), Nat (Natura), Bia (Bradesco), Aura (Vivo), Mara (Amaro), Elô (Cielo), Sam
(Samsung), Ully (Ultragaz). **Todas mulheres** — e isso já virou crítica pública
([Forbes, jan/2024](https://forbes.com.br/forbes-mulher/2024/01/por-que-os-avatares-das-empresas-sao-sempre-mulheres/)):
a crítica é que a IA de serviço sempre ser mulher reencena a secretária. Como o nome CintIA
já está decidido (nome próprio), a escolha está feita; o ponto fica registrado para você saber
que existe e não ser pega de surpresa se alguém levantar.

A referência mais próxima do que a CintIA precisa é a **Nat, da Natura**: mulher negra
brasileira, renderizada em 3D estilizado — não fotorrealista, não desenho infantil. Calorosa,
adulta, reconhecível em miniatura.

A **Lu do Magalu** foi para o outro extremo: em 2024 virou Unreal Engine 5, pele e roupa
fotorrealistas ([Canaltech](https://canaltech.com.br/e-commerce/nova-lu-do-magalu-usou-ia-e-unreal-engine-5-para-ficar-mais-realista-294489/)).
É orçamento de varejista bilionária, e o ganho disso some num círculo de 48px.

### 2. A literatura de UX diz para NÃO ficar no meio do caminho

Pesquisa de 2022–2026 sobre vale da estranheza em chatbot
([Taylor & Francis](https://www.tandfonline.com/doi/full/10.1080/10447318.2022.2121038),
[Springer](https://link.springer.com/chapter/10.1007/978-3-032-30860-3_12)):

- Avatar **hiper-realista causa mais estranheza** que avatar cartunizado ou estático.
- O que mais incomoda não é o realismo em si: é a **incoerência** entre a cara do avatar e o
  que ele demonstra saber.
- A conclusão prática: *se você não consegue chegar no fotorrealismo de verdade, não mire no
  meio* — um personagem claramente ilustrado funciona melhor que uma "pessoa real" levemente
  errada.

Rosto gerado por IA entra exatamente nesse meio: parece foto até alguém olhar a mão, o brinco
ou o fundo. E um print disso circulando num grupo de compradores é risco de reputação.

### 3. A própria spec da CintIA já fechou essa porta

Regra de honestidade, seção 1 da jornada: *"A CintIA é uma assistente, com nome e
personalidade — não uma pessoa fingindo ser humana."* Uma foto realista de uma mulher que não
existe contradiz a regra antes da primeira mensagem. O vínculo, como a própria spec diz, vem
do nome, do tom e de ela resolver rápido.

Some-se a isso que a Meta restringiu assistentes de IA de propósito geral no WhatsApp a partir
de 15/01/2026 — uso de negócio continua liberado, mas o perfil não pode se passar por atendente
humano.

### 4. Traços brasileiros: por que ilustração ajuda aqui

O banco de imagens gratuito **não tem farmácia brasileira com gente dentro** (já levantado em
set/2026, 15 fotos aproveitadas de 41). Em ilustração você controla o tom de pele e o cabelo
diretamente — por isso as opções vêm em 4 combinações de pele e cabelo, e não numa só.

---

## Como foi desenhado

- **Rosto grande no quadro.** O que decide é o corte circular de 48px da lista de conversas,
  não o perfil aberto. Cabeça ocupa ~60% da altura.
- **Silhueta de cabelo escuro sobre magenta.** É o que identifica a CintIA em miniatura. Nenhum
  texto sobrevive a 48px — por isso não tem nome nem logo na imagem.
- **Adulta, não fofa.** Sem olho gigante, sem diminutivo visual. A regra de tom da spec
  ("espontâneo, não infantil") vale para o desenho também: quem olha é dono de farmácia de
  30 anos de rua.
- **Paleta da marca no fundo, nunca na pele.** Magenta #DC36C0 (`--magenta-500`) e
  #F9C0EA (`--magenta-100`). Amarelo fica de fora — o manual proíbe magenta e amarelo em áreas
  grandes juntos.

⚠️ **O manual da marca [Empresa] não tem seção de ilustração/personagem** — mesma lacuna do
co-branding. Proporção, traço e tom de pele aqui são decisão nossa, não do manual.

---

## Especificação técnica do WhatsApp Business

- Formato JPG ou PNG · mínimo 192×192 · **recomendado 640×640** · máx. 5 MB.
- Os arquivos saem em 1024×1024 (dá margem; o WhatsApp reduz).
- O corte é **circular**: o que estiver nos cantos do quadrado some.

---

## Como gerar outra combinação

Abre no Chrome e troca os parâmetros:

```
cintia-avatar.html?pele=media&cabelo=cacheado&fundo=magenta
```

| Parâmetro | Valores |
|---|---|
| `pele` | `clara` · `media` · `escura` · `retinta` |
| `cabelo` | `cacheado` · `ondulado` |
| `cor` | `preto` · `castanho` |
| `fundo` | `magenta` · `claro` · `escuro` |

Para exportar em PNG (Chrome headless):

```
"C:\Program Files\Google\Chrome\Application\chrome.exe" --headless --disable-gpu ^
  --screenshot="saida.png" --window-size=1024,1024 ^
  "cintia-avatar.html zap/avatar-cintia/cintia-avatar.html?pele=media&cabelo=cacheado&fundo=magenta"
```

⚠️ **O Chrome cacheia arquivo `file://`.** Depois de editar o HTML, renomeie o arquivo ou
acrescente `&t=123` na URL, senão ele renderiza a versão antiga sem avisar.

**Sempre rodar `teste-corte.html` antes de subir.** Avatar que funciona a 200px pode virar
borrão a 48px, que é onde a farmácia vê.

---

## Se um dia quiser testar a versão 3D (caminho da Nat)

Não é para a v1 — fica registrado. O que mudaria: personagem em 3D estilizado, mesma cara,
com volume e luz. Precisa de ilustrador ou de geração por IA com revisão humana, e **continua
valendo a regra**: estilizado, nunca fotorrealista. O ganho real não é o avatar bonito, é poder
reusar o mesmo personagem em anúncio, site e e-mail — que é o que a Natura e a Magalu fazem.

Relacionado: `../cintia-ura-whatsapp.md` · `../cintia-faq.md` · `../cintia-benchmark.md`
