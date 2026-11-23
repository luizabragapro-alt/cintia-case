# O prompt do rosto da CintIA

> Calibrado em 09/10/2026 depois de 8 gerações. O que está aqui são as regras que
> **mudaram o resultado**, não teoria.

## A referência: Mavi (@sou.mavi)

A Mavi é a agente autônoma de uma varejista. O que importa na referência **não é o
cabelo ruivo nem a pele dela** — é a proposta:

- **Personagem de animação 3D**, estilo filme da Pixar. Não é foto, não é desenho chapado.
- **Adulta e profissional.** Blazer, postura, expressão de quem resolve. Não é modelo.
- Ela **se assume personagem**. É isso que tira o ar de "foto de banco de imagem".

É esse o alvo. Com as características da CintIA, que são outras.

## O que a CintIA precisa ser

| | |
|---|---|
| Idade | **35 a 50 anos.** Esse é o requisito que mais custou a sair |
| Por quê | O público é dono de farmácia independente, gente mais da antiga. Rosto de 25 anos não conversa com ele |
| Traços | Brasileira, pele morena, olhos e cabelo escuros |
| Expressão | Acolhedora e confiante. Sorriso de boca fechada ou leve |
| Roupa | Discreta, gola alta, abotoada. **Nada de decote, ombro de fora ou regata** |
| Enquadramento | Só cabeça e ombros, rosto preenchendo o quadro, mãos vazias |
| Fundo | **Liso, claro e sem cenário** |

## O prompt

```
stylized 3D animated character portrait, animation film style,
Brazilian Latina woman, 45 years old, warm brown skin, dark brown eyes,
dark brown hair with a few grey strands, shoulder length,
visible wrinkles and deep smile lines,
kind confident closed mouth smile,
modest blouse buttoned to the neck,
tight headshot, face fills the frame, head and shoulders only, empty hands,
isolated on plain white background, flat even studio lighting,
centered front view
```

## A ordem das palavras importa mais que as palavras

O gerador dá mais peso ao **começo** do prompt. Com `stylized 3D animated character` na
frente, ele gastava a atenção no estilo e devolvia rosto sério, de traço asiático e com
decote — ignorando sorriso, idade e roupa.

Versão com o que importa na frente:

```
smiling Afro Brazilian woman 45 years old, big warm friendly smile,
3D animated movie character, Pixar animation style,
brown skin, dark curly hair with grey strands,
laugh lines and wrinkles around the eyes, full lips, broad nose,
white collared shirt buttoned up,
head and shoulders portrait, plain white background, flat studio lighting
```

Duas trocas deliberadas:

- **`smiling` como primeira palavra.** `kind confident closed mouth smile` no meio do
  prompt virava cara séria em toda geração.
- **`Afro Brazilian` em vez de `Brazilian Latina`.** `Latina` não tirava o rosto do
  padrão asiático. `Afro Brazilian` + `full lips` + `broad nose` move de verdade — e
  bate com a regra de banco de imagem que já vale aqui: traços brasileiros, para não
  ficar distante de quem olha.

## As quatro armadilhas (todas custaram uma geração)

1. **O gerador puxa tudo para 25 anos e para "bonita".** Número de idade sozinho não
   resolve. O que resolve é pedir o **sinal visual**: `a few grey strands`,
   `visible wrinkles and deep smile lines`. Sem isso volta sempre jovem.

2. **Mas não exagere no sinal.** `silver grey streaks` + `50 years old` devolveu uma
   senhora de cabelo todo branco. E `reading glasses` fez ela **literalmente segurar um
   livro**. Se quiser óculos, peça `glasses` e acrescente `empty hands`.

3. **Ele ignora roupa e cor de fundo.** Pedi jaleco: veio blusa. Pedi fundo magenta:
   veio cinza. Por isso o fundo é trocado pelo template, e jaleco e crachá, se um dia
   voltarem, são desenhados por ele.

4. **O fundo da origem decide se o recorte funciona.** O template troca o fundo por
   preenchimento a partir das bordas, então ele precisa de **fundo claro e liso**.
   Fundo escuro com vinheta encosta no tom do cabelo e o recorte come metade do rosto —
   aconteceu. Fundo com cenário não recorta de jeito nenhum.
   Se o fundo da origem for escuro, baixe `lum`; se comer o cabelo, suba de volta.

## Traços brasileiros: o teto do gerador gratuito

Mesmo com `Brazilian Latina` o rosto puxa para traços asiáticos. Insistir em
`warm brown skin`, `dark brown eyes` e `full lips` melhora, mas não resolve sempre.
É limitação do modelo grátis (`sana` no pollinations.ai), não do prompt.

Num gerador pago (ChatGPT, Gemini, Midjourney) o mesmo prompt entrega melhor, em 1024×1024
e sem marca d'água. O template continua servindo para recorte e fundo.

## Depois de gerar

1. Jogue o `.jpg` em `faces/`
2. `3. Copie um `examples/cintia-avatar-*.json`, troque `rosto` pelo nome do arquivo
4. `5. **Confira o corte circular antes de subir** — é em 48px que a farmácia vê
