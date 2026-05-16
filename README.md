# 🎯 SM2 - Laboratório de Classificação Visual e Ética em IA

---

## 📋 Parte 1 — Laboratório de Classificação Visual

### Definição de Categorias
O modelo foi treinado com duas classes de classificação:
- **Tênis Originais**
- **Tênis Falsos**

### Alimentação de Dados
Foram carregadas **20 imagens para cada categoria**, utilizando 
deliberadamente um dataset enviesado — as imagens de tênis originais 
apresentavam padrões visuais distintos dos falsos, como ângulos, 
iluminação e contexto específicos, limitando a capacidade de 
generalização do modelo.

### Teste de Inferência e Registro do Erro

<img width="1346" height="636" alt="image" src="https://github.com/user-attachments/assets/0a1f0c76-89a9-44dd-b7c8-24fb944d02b4" />

<img width="1333" height="614" alt="image" src="https://github.com/user-attachments/assets/3a577c32-1da2-4bb1-94d2-3acd3905d1c4" />


> ⚠️ **Erro registrado:** Um tênis **original** (Adidas branco) foi 
> classificado pelo modelo com **98% de confiança** como **tênis falso** 
> — um falso positivo gerado pelo viés do dataset de treinamento.

---

## 🧠 Parte 2 — Memorial de Impacto e Ética

### 1. Mecanismo do Viés
A seleção restrita de dados corrompe a lógica do algoritmo porque o 
modelo aprende apenas os padrões presentes no conjunto de treinamento, 
e não a realidade em sua totalidade. Quando o dataset apresenta apenas 
imagens de tênis originais em condições específicas de ângulo, 
iluminação e contexto, o algoritmo associa essas características 
superficiais à classe "original" — e não os atributos reais de 
autenticidade. Assim, qualquer imagem que fuja desse padrão visual, 
mesmo sendo genuína, gera uma visão distorcida da realidade e é 
classificada incorretamente.

### 2. Consequência Social
O impacto de um sistema enviesado vai além do erro técnico. No contexto 
de autenticação de produtos, um indivíduo que tem seu tênis legítimo 
classificado como falso sofre consequências diretas: perde credibilidade, 
enfrenta constrangimento público e tem seu patrimônio questionado sem 
justificativa real. O sistema invisibiliza sua verdade e impõe um 
julgamento automatizado que marginaliza quem não se encaixa nos padrões 
arbitrários definidos pelo dataset — revelando que o algoritmo reproduz 
e amplifica os preconceitos de quem o treina.

### 3. Ação Mitigadora — Human-in-the-loop
A intervenção proposta garante que nenhuma classificação de alto impacto 
seja tomada de forma totalmente automatizada. No processo de curadoria, 
um auditor humano revisa obrigatoriamente os casos limítrofes — aqueles 
com confiança abaixo de 90% — antes de qualquer decisão final. Além 
disso, o dataset passa por revisão periódica com especialistas que 
identificam lacunas de representatividade, inserindo imagens de contextos 
variados para reduzir o viés. Essa abordagem assegura que a equidade 
não é tratada como etapa opcional, mas como parte estrutural do pipeline 
de desenvolvimento do modelo.

---

## 🛠️ Tecnologias e Ferramentas

- **Teachable Machine** (Google) — treinamento do modelo de visão computacional
- **Webcam / Upload de imagens** — captura do dataset
- **Modelo de classificação de imagens** — inferência em tempo real
