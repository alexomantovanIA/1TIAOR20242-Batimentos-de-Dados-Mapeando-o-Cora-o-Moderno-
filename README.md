# FIAP - Faculdade de Informática e Administração Paulista

<p align="center">
<a href="https://www.fiap.com.br/"><img src="assets/logo-fiap.png" alt="FIAP - Faculdade de Informática e Administração Paulista" border="0" width="40%" height="40%"></a>
</p>

---

# Batimentos de Dados – Mapeando o Coração Moderno

### Fase 1

---

## 👨‍🎓 Integrantes:

- [Alexandre Oliveira Mantovani](https://www.linkedin.com/in/alexomantovani)
- [Edmar Ferreira Souza](https://www.linkedin.com/in/)
- [Ricardo Lourenço Coube](https://www.linkedin.com/in/ricardolcoube/)
- [Jose Andre Filho](https://www.linkedin.com/in/joseandrefilho)

## 👩‍🏫 Professores:

- Tutor: [Leonardo Ruiz Orabona](https://www.linkedin.com/in/leonardoorabona)
- Coordenador: [André Godoi](https://www.linkedin.com/in/profandregodoi)

---

## 📌 Descrição do Projeto

Este repositório contém a **Fase 1 – Batimentos de Dados** do projeto **CardioIA**, cuja visão é construir uma plataforma acadêmica que simule um ecossistema de cardiologia moderna integrando **IoT**, **Machine Learning**, **NLP** e **Visão Computacional** para fins **educacionais** (triagem, apoio a diagnóstico, monitoramento e previsão).  

Nesta fase, atuamos como *cientistas de dados hospitalares* para **levantar, organizar e entender** três bases fundamentais que alimentarão as próximas etapas:  
1) **Dados Numéricos** (ex.: idade, pressão arterial, colesterol, frequência cardíaca, comorbidades);  
2) **Textos** em `.txt` (ex.: materiais técnicos/literários sobre saúde cardiovascular);  
3) **Imagens** (ex.: traçados de ECG) para tarefas de visão computacional.

> **Aviso de Governança & Ética (LGPD)**: todos os dados utilizados aqui são **públicos, anonimizados** ou **sintéticos**; este repositório tem **uso estritamente acadêmico** e **não** substitui decisões clínicas.

---

## 📦 Entregáveis

### 📊 Parte 1 — Dados Numéricos (IoT)
- **Link para download (Drive/OneDrive)**: **[INSERIR_LINK_PUBLICO]**
- **Formato**: `.csv` e/ou `.xlsx` (≥ 100 linhas)
- **Origem**: dados **sintéticos** gerados via `scripts/gerar_dados_numericos.py` *(ou substitua por base pública com citação)*
- **Variáveis sugeridas (exemplos)**:  
`idade`, `sexo`, `imc`, `pressao_sistolica`, `pressao_diastolica`, `ldl`, `hdl`, `triglicerides`, `colesterol_total`, `freq_cardiaca`, `fumante`, `diabetes`, `historico_familiar`, `sintoma_dor_toracica`, `alvo_doenca_cardiaca`.

**Dicionário de dados (resumo):**

| Variável | Tipo | Unidade | Justificativa clínica |
|---|---|---|---|
| idade | int | anos | risco cardiovascular aumenta com a idade |
| sexo | categórica | — | diferenças epidemiológicas |
| pressao_sistolica/diastolica | int | mmHg | hipertensão = fator de risco |
| ldl/hdl/colesterol_total | int | mg/dL | perfil lipídico e risco aterosclerótico |
| triglicerides | int | mg/dL | componente metabólico relevante |
| imc | float | kg/m² | obesidade e risco |
| fumante/diabetes/historico_familiar | binária | — | fatores clássicos de risco |
| freq_cardiaca | int | bpm | sinal fisiológico útil na triagem |
| sintoma_dor_toracica | binária | — | triagem clínica |
| alvo_doenca_cardiaca | binária | — | rótulo didático p/ modelos |

---

### 📝 Parte 2 — Dados Textuais (NLP)
- **Arquivos**: `docs/textos/texto_01.txt`, `docs/textos/texto_02.txt` *(≥ 2 textos)*  
- **Fontes & Licenças**: ver `docs/fontes_e_licencas.md`  
- **Possíveis usos**: classificação de tópicos (prevenção/diagnóstico/tratamento), **extração de sintomas** (NER), análise de sentimentos, **sumarização** de protocolos.

---

### 🖼️ Parte 3 — Dados Visuais (VC)
- **Tipo sugerido**: **ECG** (≥ 100 imagens `.png` ou `.jpg`)  
- **Link para download (Drive/OneDrive)**: **[INSERIR_LINK_PUBLICO]**  
- **Amostras**: opcionalmente inclua 4–6 imagens em `samples/imagens_sample/`  
- **Possíveis usos**: detecção de padrões (QRS), **reconhecimento de anomalias**, extração de características (FFT, bordas, textura).  
- **Alternativa**: gerar ECGs sintéticos com `scripts/gerar_ecg_sintetico_em_imagens.py`.

---

### 🔧 Scripts inclusos
- `scripts/gerar_dados_numericos.py` – gera CSV/XLSX sintético realista (≥ 500 linhas).  
- `scripts/exemplo_nlp.py` – exemplo didático de tópicos (LDA) e extração simples de sintomas.  
- `scripts/gerar_ecg_sintetico_em_imagens.py` – cria 100 PNGs de ECG sintético.

> **Recomendação**: mantenha no repositório apenas **amostras**; hospede os conjuntos completos no **Drive/OneDrive** e referencie o **link público** no README.

---

## 🧪 Metodologia

1. **Aquisição/Geração de Dados**: uso de fontes públicas anonimizadas e/ou geração sintética controlada.  
2. **Limpeza & Padronização**: normalização de tipos, unidades e codificação (`UTF-8`); checagem de nulos e outliers.  
3. **Governança & Documentação**: registro de **origem**, **licenças**, **limitações** e **viés potencial**.  
4. **Publicação**: arquivos grandes em **Drive/OneDrive** com permissão *“qualquer pessoa com o link pode visualizar”*.  
5. **Validação**: amostras no repo, abertura em Excel/Sheets e testes de leitura por scripts.  

---

## 📈 Visualizações (Exemplos sugeridos)
- Histogramas de `pressao_sistolica`, `ldl`, `imc` e `freq_cardiaca`.  
- Curvas exemplo de ECG (normais x com *artefatos*).  
- **NLP**: *wordcloud* de termos e tópicos principais por LDA.  

*(As figuras serão adicionadas nas próximas fases conforme análises forem realizadas.)*

---

## 📊 Métricas (a acompanhar nas próximas fases)
- **Base numérica**: métricas de um baseline (ex.: regressão logística) para previsão de `alvo_doenca_cardiaca` — *acurácia, F1, AUC*.  
- **NLP**: *coherence score* para tópicos; precisão de extração de entidades (quando houver *gold standard*).  
- **Visão**: acurácia/ROC para classificar ECGs (normal vs anômalo) em *hold-out* didático.

---

## 🗂️ Estrutura do Projeto

```
📦 1TIAOR20242-Batimentos-de-Dados-Mapeando-o-Cora-o-Moderno
│
├─ docs/                
│   ├─ textos/
│   │   ├─ texto_01.txt
│   │   └─ texto_02.txt
│   └─ fontes_e_licencas.md
├─ scripts/
│   ├─ 
│   ├─ 
│   └─ 
├─ samples/             
│   ├─ exemplo_sample.csv 
│   └─ imagens_sample/  
├─ .gitignore
└── requirements.txt
```

---

## ✅ Requisitos para Execução

- Python **3.10+**
- (Opcional) Jupyter Notebook ou Google Colab

```bash
pip install -r requirements.txt
```

**Exemplo de `requirements.txt`** (sugerido):
```
numpy
pandas
matplotlib
scikit-learn
```
> Adicione bibliotecas extras conforme sua evolução (ex.: `spacy`, `pillow`, `opencv-python`).

---

## 🔍 Checklist Rápido (antes de enviar)

- [ ] CSV/XLSX com **≥ 100 linhas** e **link público** testado.  
- [ ] **2 textos `.txt`** em `docs/textos/` + `docs/fontes_e_licencas.md`.  
- [ ] **100 imagens** no Drive/OneDrive + 4–6 amostras em `samples/`.  
- [ ] **Dicionário de dados** e **racional clínico** descritos acima.  
- [ ] Scripts funcionais em `scripts/` e instruções de execução.  
- [ ] Avisos de **LGPD/ética** e finalidade **acadêmica**.

---

## 📝 Licença

<p xmlns:cc="http://creativecommons.org/ns#" xmlns:dct="http://purl.org/dc/terms/">
Este projeto segue o modelo FIAP e está licenciado sob 
<a href="http://creativecommons.org/licenses/by/4.0/?ref=chooser-v1" target="_blank" rel="license noopener noreferrer">Attribution 4.0 International (CC BY 4.0)</a>.
</p>
