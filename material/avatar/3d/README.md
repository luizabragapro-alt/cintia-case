# CintIA 3D — o avatar que foi para o WhatsApp

> Feito em 09/10/2026, depois que a versão ilustrada ficou cartoon demais.
> **Critério da Luiza:** tem que parecer uma pessoa, e uma pessoa que entende de farmácia.

## ⚠️ Estado em 09/10/2026: a cara ainda não passou

A Luiza recusou a primeira leva: **jovial e sexualizada demais**. O público é dono de
farmácia independente, gente mais da antiga — o rosto precisa ter **35 a 50 anos**.
Referência de proposta: **Mavi (@sou.mavi)**, personagem de animação 3D, adulta e
profissional. O prompt calibrado e as armadilhas estão em `PROMPT.md`.

Também por decisão dela, **o jaleco branco e o crachá magenta saíram** (`jaleco:false`,
`cracha:false`, agora o padrão do template). Primeiro a cara; roupa depois.

O que ficou de pé: `cintia-40anos-tentativa.png` é a tentativa mais próxima — a idade
chegou perto dos 40 e o ar de modelo sumiu, mas a expressão ficou dura e os traços ainda
não são brasileiros. **Não é para subir.**

## Como a peça é montada

Um gerador de peças interno recorta o rosto, troca o fundo pela cor da marca e desenha
o jaleco branco e o crachá. O crachá não tem texto nem logo: em 48px nada disso seria
legível, e ele existe para o perfil aberto.

## De onde veio o rosto

Gerado em `pollinations.ai` (endpoint público, sem login, modelo `sana`), em 09/10/2026.
Os originais estão aqui como `_origem-*.jpg`.

**Três coisas para saber antes de usar comercialmente:**

1. **O serviço gratuito marca a imagem** no canto inferior direito. O enquadramento do
   template corta a marca d'água — confira sempre que mudar o recorte.
2. **Confirme a licença de uso** do gerador antes de o avatar virar peça pública. Eu não
   verifiquei isso.
3. **O gerador ignorou "jaleco"** e ignorou "fundo magenta". Por isso as duas coisas são
   desenhadas pelo template, não pedidas no prompt. Ele também puxa o rosto para traços
   asiáticos: foi preciso insistir em "Brazilian Latina, full lips, tan brown skin".

Prompt que funcionou:

> close-up headshot, 3D stylized character render, Brazilian Latina woman, 34 years old,
> friendly confident smile, dark brown eyes, full lips, tan brown skin, dark brown curly hair,
> wearing a white pharmacist lab coat over a shirt, head and shoulders only, plain solid light
> gray studio background, Pixar style stylized realism, soft key light, centered front view,
> high detail

**Fundo cinza liso é de propósito:** é o que o template consegue recortar. Se você gerar um
rosto com fundo colorido ou com cenário, a troca de fundo não funciona.

Se um dia rodar num gerador pago (ChatGPT, Gemini, Midjourney), use o mesmo prompt pedindo
1024×1024 — a qualidade sobe e não vem marca d'água. O template continua servindo para o
recorte, o fundo e o jaleco.

## A versão ilustrada

Ficou na pasta de cima (`../cintia-A.png` … `../cintia-D.png`) junto com a pesquisa de
mercado que a originou. Não foi descartada por estar errada: foi descartada porque o critério
mudou para "tem que parecer gente".
