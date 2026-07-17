# ⚽ Machine Learning no Futebol Feminino 🇧🇷
### Dois projetos de previsão (*forecasting*) para o Ensino Médio

Bem-vindo(a)! Aqui você encontra **dois projetos completos** de Machine Learning,
feitos para estudantes do ensino médio aprenderem a **prever resultados de futebol**
usando dados reais.

> ⚠️ **Só futebol feminino!** Todos os dados são de partidas **femininas**
> internacionais. Os jogos masculinos foram **totalmente excluídos**.

---

## 📁 O que tem nesta pasta

| Arquivo | O que é |
|---|---|
| `Projeto_1_Quem_vai_vencer_CLASSIFICACAO.ipynb` | Prever **quem vence** (casa / empate / visitante) → **classificação** |
| `Projeto_2_Quantos_gols_REGRESSAO.ipynb` | Prever **quantos gols** / o **placar** → **regressão** |
| `dados/jogos_femininos.csv` | 5.657 jogos internacionais femininos (1969–2023) |
| `LEIA-ME.md` | Este arquivo |

---

## 🎯 Os dois projetos

### Projeto 1 — Quem vai vencer? (Classificação)
- **Pergunta:** o jogo termina em vitória da casa, empate ou vitória da visitante?
- **Ideia principal:** transformar cada seleção em uma "nota de força" com o
  **rating Elo** (o mesmo do xadrez), calculado ao longo do tempo.
- **Modelos:** Regressão Logística e Random Forest.
- **Resultado:** ~**70% de acerto**, contra ~50% de um "chute básico".
- **Final:** o modelo prevê os jogos da **Seleção Brasileira** 🇧🇷.

### Projeto 2 — Quantos gols? (Regressão)
- **Pergunta:** quantos gols cada time vai marcar? Qual o **placar provável**?
- **Ideia principal:** juntar o rating Elo com a **forma recente** (média de gols
  marcados e sofridos nos últimos jogos).
- **Modelos:** Regressão Linear, Random Forest e Gradient Boosting.
- **Resultado:** erra em média **~1,3 gol** por jogo (baseline erra ~1,9).
- **Final:** uma função `prever_placar("Brazil", "Argentina")` que estima o placar!

---

## 🧠 Conceitos de ML que você vai aprender

1. **Classificação x Regressão** — prever categorias x prever números.
2. **Engenharia de atributos** — criar informações úteis (Elo, forma recente).
3. **Divisão treino/teste CRONOLÓGICA** ⏳ — treinar com o **passado** e testar no
   **futuro**, porque os dados têm datas. *Nunca* embaralhamos o tempo!
4. **Vazamento de dados (*data leakage*)** — por que não podemos usar o futuro para
   prever o passado, e como evitamos isso.
5. **Baseline** — sempre comparar o modelo com uma regra simples.
6. **Métricas** — Acurácia e Matriz de Confusão (Projeto 1); MAE e RMSE (Projeto 2).

---

## ▶️ Como executar

Você precisa de Python com estas bibliotecas (todas gratuitas):

```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

Depois, na pasta do projeto:

```bash
jupyter notebook
```

E abra um dos arquivos `.ipynb`. Rode as células de cima para baixo
(tecla **Shift + Enter**). Cada projeto é **independente** — pode começar por qualquer um,
mas sugerimos o **Projeto 1** primeiro.

> 💡 Também funciona no **Google Colab**: basta enviar o `.ipynb` e a pasta `dados/`.

---

## 📊 Sobre os dados

- **Fonte:** projeto *FootballTournamentPrediction* do **Alan Turing Institute**
  (dados públicos de resultados internacionais do futebol feminino).
- **Período:** novembro/1969 a agosto/2023.
- **209 seleções** e **5.657 partidas**.
- Colunas: data, time da casa, time visitante, gols de cada lado, torneio e se o
  jogo foi em campo neutro.

---

## 🚀 Desafios extras

Cada notebook termina com uma lista de **exercícios** para você modificar o código,
testar novas ideias e ver como os resultados mudam. Divirta-se — e lembre-se:
Machine Learning **não é uma bola de cristal**, é uma ferramenta para estimar
**probabilidades** a partir do que já aconteceu! ⚽📈
