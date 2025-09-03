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
- **Arquivos** `samples/tabelas_sample/base_cardiaca.xlsx`
- **Link para download (Drive/OneDrive)**: **[https://docs.google.com/spreadsheets/d/1L95psjpKOSCRISwpy52hlgUXfQptkgSF/edit?gid=1256256245#gid=1256256245]**
- **Formato**: `.csv` e/ou `.xlsx` (≥ 100 linhas)
- **Origem**: Dados simulados

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
- **Arquivos**: `docs/textos/doppler_fluxo_sanguineo.txt`, `docs/textos/imagiologia_cardiovascular.txt`
- **Fontes & Licenças**: ver `docs/textos/Cap 1 - Batimento de dados`
- **Possíveis usos**: classificação de tópicos (prevenção/diagnóstico/tratamento), **extração de sintomas** (NER), análise de sentimentos, **sumarização** de protocolos.

---

### 🖼️ Parte 3 — Dados Visuais (VC)

- **Tipo**: **ECG** (944 imagens`.jpg`)  
- **Link para download (Google Drive)**: [**https://drive.google.com/drive/folders/1QFmSOT5SL0NrG7mY9n-_CrEzSdFGWnBq?usp=sharing**]
- **Amostras locais**: `samples/imagens_sample/` (4 exemplos)
- **Documentação completa**: `samples/images_sample/link_imagens_completas.md`

**Dataset características:**
- Origem: data.mendeley.com
- Aplicação: Classificação e detecção de anomalias por IA
- Formato padronizado para análise computacional
- Dados anonimizados e de uso acadêmico

**Análises previstas (próximas fases):**
- Pré-processamento e normalização de imagens
- Extração de características (bordas, texturas, padrões)
- Treinamento de CNN para classificação automática
- Métricas: acurácia, sensibilidade, especificidade

---

## 🧪 Metodologia

1. **Aquisição/Geração de Dados**: uso de fontes públicas anonimizadas e/ou geração sintética controlada.  
2. **Limpeza & Padronização**: normalização de tipos, unidades e codificação (`UTF-8`); checagem de nulos e outliers.  
3. **Governança & Documentação**: registro de **origem**, **licenças**, **limitações** e **viés potencial**.  
4. **Publicação**: arquivos grandes em **Drive/OneDrive** com permissão *“qualquer pessoa com o link pode visualizar”*.  
5. **Validação**: amostras no repo, abertura em Excel/Sheets e testes de leitura por scripts.  

---

## 📈 Visualizações
- Histogramas de `pressao_sistolica`, `ldl`, `imc` e `freq_cardiaca`.  
- Curvas exemplo de ECG (normais x com *artefatos*).
- **NLP**: *wordcloud* de termos e tópicos principais por LDA.  

*(As figuras serão adicionadas nas próximas fases conforme análises forem realizadas.)*

---

## 📊 Métricas
- **Base numérica**: métricas de um baseline (ex.: regressão logística) para previsão de `alvo_doenca_cardiaca` — *acurácia, F1, AUC*.  
- **NLP**: *coherence score* para tópicos; precisão de extração de entidades (quando houver *gold standard*).  
- **Visão**: acurácia/ROC para classificar ECGs (normal vs anômalo) em *hold-out* didático.

---

## 🗂️ Estrutura do Projeto

```
📦 1TIAOR20242-Batimentos-de-Dados-Mapeando-o-Cora-o-Moderno
│
├─ assets/
│   └─ logo-fiap.png
├─ docs/
│   └─ textos/
│       ├─ Cap 1 - Batimento de dados.pdf
│       ├─ doppler_fluxo_sanguineo.txt
│       └─ imagiologia_cardiovascular.txt
├─ samples/
│   ├─ imagens_sample/
│   │   ├─ ECG_HB.jpg
│   │   ├─ ECG_MI.jpg
│   │   ├─ ECG_Normal.jpg
│   │   └─ ECG_PMI.jpg
│   └─ tabelas_sample/
│       └─ base_cardiaca.xlsx
├─ README.md
└─ requirements.txt
```

---

## ✅ Requisitos para Execução

- Python **3.10+**

```bash
pip install -r requirements.txt
```

**Exemplo de `requirements.txt`** (sugerido):
```

```
---

## 📝 Licença

<p xmlns:cc="http://creativecommons.org/ns#" xmlns:dct="http://purl.org/dc/terms/">
Este projeto segue o modelo FIAP e está licenciado sob 
<a href="http://creativecommons.org/licenses/by/4.0/?ref=chooser-v1" target="_blank" rel="license noopener noreferrer">Attribution 4.0 International (CC BY 4.0)</a>.
</p>
