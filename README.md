# O Grand Slam das Seleções — versão notebook

Reconstrução em código (pandas + Python) do ranking das 5 campanhas campeãs do Brasil na Copa do Mundo, originalmente publicado como README + infográfico em PDF sem dado bruto versionado.

## O que mudou em relação à v5 (PDF)

- Implementa a metodologia como função Python reutilizável
- Reconstrói o jogo a jogo de cada uma das 5 campanhas (adversário, gols, fase) — 1958, 1970 e 1962 batem **exatamente** com o Ataque/Defesa/Score publicados na v5
- **Corrige uma divergência histórica real que estava nos dados da v5:** a campanha de 1994 tratava a Holanda como semifinalista, mas historicamente ela foi eliminada nas quartas de final — pelo próprio Brasil. Corrigido nesta versão: o score de 1994 passa de 18,5 para **17,5** (não muda a posição no ranking). Ver seção 4 do notebook.
- 2002 tem um resíduo pequeno (~1,5 pt no ataque, sem afetar a colocação) que não foi possível rastrear — todos os 7 placares e fases de adversário foram conferidos contra múltiplas fontes e batem; documentado como pendente em vez de forçar um ajuste sem base

## Estrutura

```
grand_slam_selecoes/
├── README.md
├── requirements.txt
├── data/
│   ├── jogos_v5_oficial.csv          # jogo a jogo das 5 campanhas
│   └── campanhas_v5_oficial.csv      # resultado agregado publicado na v5
└── notebooks/
    └── 01_ranking_selecoes.ipynb
```

## Status

- [x] Reconstrução da metodologia em código
- [x] Jogo a jogo de todas as 5 campanhas
- [x] Validação: 3 de 5 campanhas batem exatamente com o score publicado
- [x] Divergência histórica de 1994 (Holanda) encontrada e corrigida (18,5 → 17,5)
- [ ] Resíduo de 2002 (~1,5 pt) permanece sem explicação encontrada — documentado, não forçado
- [x] Infográfico v6 em PDF gerado, com o dado corrigido de 1994

## Infográfico (v6)

`infografico/grand-slam-selecoes-v6.pdf` — mesmo estilo visual do infográfico original, já com a correção da Holanda/1994. Fonte editável em `infografico/grand-slam-selecoes-v6.html`.
