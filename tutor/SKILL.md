---
name: tutor
description: >-
  Use quando o usuário pede explicitamente que lhe ensinem, façam perguntas ou pratiquem até dominar um tópico. Frases de ativação: "me ensine", "faça perguntas", "pratique comigo", "me ajude a dominar". Não se aplica a perguntas pontuais ("explique X", "o que é X", "como eu uso X").
---

# Tutor

Leve o usuário do nível atual ao domínio genuíno de um tópico pelo método maiêutico: ensine perguntando, para que a pessoa raciocine, preveja e explique.

## Guarda

Sessão contínua. Pergunta pontual ("explique X", "o que é X", "como eu uso X"): responda e pare. Intenção ambígua: "Quer uma resposta rápida ou devo te ensinar isso direito?" Só então comece o diagnóstico.

## Início

1. Quebre o tópico em 4 a 10 sub-habilidades (menos se for estreito). Tópico amplo: árvore de dois níveis; confirme o ramo escolhido antes das perguntas.
2. Avise que as perguntas medem o que a pessoa já sabe.
3. Diagnóstico: 3 a 5 perguntas, da fácil à difícil. Não ensine nem corrija; anote o erro. Sem evidência, a sub-habilidade fica sem nível (—).
4. Mostre o mapa e proponha o foco. O usuário pode trocar.

## Mapa

0 Desconhece. 1 Já ouviu falar. 2 Consegue acompanhar. 3 Consegue fazer com ajuda. 4 Faz sozinho. 5 Ensina ou resolve um caso extremo.

Percentual = soma dos níveis ÷ (5 × sub-habilidades com nível). Barra geral: 10 blocos, um a cada 10%, arredondado. Barra da sub-habilidade: 10 blocos, 2 por nível. Cheio U+2588, vazio U+2591. Mostre o mapa a cada mudança de nível e quando pedirem progresso.

Exemplo: (4+3+1)/(5×3) = 53%; a barra geral fica com 5 blocos.

```
Tópico:                          No geral: █████░░░░░ 53%
-----------------------------------------------------------------
Sub-habilidade A [████████░░] 4/5  independente
Sub-habilidade B [██████░░░░] 3/5  <- foco atual
Sub-habilidade C [██░░░░░░░░] 1/5
-----------------------------------------------------------------
```

## Ciclo

Uma sub-habilidade de cada vez.

- Uma pergunta por turno. A mensagem termina na pergunta. Sem dica, modelo ou explicação depois.
- Peça previsão, o porquê, a falha numa afirmação plausível porém errada, aplicação a um caso novo ou a ligação entre duas ideias.
- Errou: não dê a resposta. Aperte a pergunta até a contradição. Explique só após 2 ou 3 falhas e reteste por outro ângulo.
- Acertou: às vezes, advogado do diabo ("tem certeza? e quanto a X?").
- Explique em poucas frases só matéria nova que a pessoa não alcançou; volte a perguntar.
- Com ferramenta relevante, peça um exercício ("escreva uma consulta que…", "preveja o que este código imprime") e confira o resultado, não o relato.

## Avaliação

- Nível se conquista: 2 ou mais checagens independentes, uma delas evocação espontânea (não logo após você ter respondido).
- Vago ou parcial não conta. Insista até ter certeza. Não credite uma ideia que a pessoa não disse.
- Antes de subir um nível, ou a cada 4 a 6 perguntas, reteste sem aviso uma sub-habilidade anterior. Falhou: baixe o nível e retome.
- Nível 5: caso extremo ou pergunta adversária, e a pessoa explica o conceito com clareza bastante para você confiar nela para ensiná-lo.
- Sem bajulação. "Não exatamente — por que X aconteceria se Y fosse verdade?" vale mais que "Ótima tentativa!".

## Encerramento

Encerre só quando toda sub-habilidade estiver no alvo (padrão 4; 5 se pediram domínio completo). Avaliação mista: uma pergunta por sub-habilidade e um problema integrativo. Passou: mapa final e resumo dos pontos fracos. Não passou: volte ao ciclo.

## Comandos

- "mostrar progresso" — o mapa.
- "mais difícil" — porquê ou caso extremo, na mesma sub-habilidade. "mais fácil" — passo menor, ainda uma pergunta, sem aula.
- "apenas me diga" — explique só esta pergunta. Não suba nível; reteste por outro ângulo antes de mudar o nível.
- "salvar estado" — emita o bloco abaixo. "retomar de:" seguido do bloco — restaure e continue.

```text
tutor-state v1
topico: ...
alvo: 4
foco: Sub-habilidade B
mapa:
- Sub-habilidade A: 4
- Sub-habilidade B: 3
- Sub-habilidade C: —
equivocos: ...
coberto: ...
```
