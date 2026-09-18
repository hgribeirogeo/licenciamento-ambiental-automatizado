# Automação Geoespacial para Licenciamento Ambiental

**Curso de Extensão — Universidade Federal de Goiás (UFG/EECA)**  
Prof. Hugo José Ribeiro

---

## Sobre o curso

Aprenda a automatizar diagnósticos ambientais para licenciamento usando Python, APIs geoespaciais públicas e dados abertos do governo federal brasileiro.

Em vez de abrir o QGIS, consultar base por base e montar tabelas manualmente, você vai construir um pipeline que:

- Consulta automaticamente UCs, Terras Indígenas, hidrografia e APP
- Extrai uso e cobertura do solo via MapBiomas (30m e 10m)
- Verifica alertas PRODES, DETER e histórico de fogo
- Gera mapas, tabelas e relatório preliminar

Tudo a partir de um único comando:

```bash
python diagnostico.py seu_empreendimento.gpkg
```

---

## Estrutura do curso

| Módulo | Conteúdo |
|---|---|
| 01 | Ambiente Colab, Google Drive e polígono de entrada |
| 02 | APIs e serviços WFS — como consultar dados geoespaciais abertos |
| 03 | Restrições legais — Unidades de Conservação e Terras Indígenas |
| 04 | Hidrografia e APP — Código Florestal automatizado |
| 05 | MapBiomas — uso e cobertura da terra, série histórica 1985–2024 |
| 06 | Pipeline completo e projeto aplicado |

**Carga horária:** 14h assíncronas + 2h clínica síncrona = 16h totais  
**Formato:** 100% online, acesso pelo Google Colab (sem instalação local)  
**Público-alvo:** consultores ambientais, analistas de órgãos ambientais, pesquisadores e estudantes de pós-graduação em ciências ambientais

---

## Como usar este repositório

Este repositório contém os **arquivos de dados** utilizados em cada módulo do curso.

Os notebooks (`.ipynb`) são disponibilizados exclusivamente na plataforma do curso após a matrícula.

### Passo a passo para cada módulo

**1.** Acesse a pasta do módulo correspondente  
**2.** Faça o download do arquivo indicado  
**3.** Faça o upload para o seu Google Drive na pasta do curso:

```
curso_licenciamento/
└── [arquivo baixado aqui]
```

O notebook de cada módulo instrui exatamente onde colocar cada arquivo.

---

## Arquivos por módulo

### Módulo 01 — Ambiente e polígono de entrada

📁 [`modulo_01/empreendimento.gpkg`](modulo_01/empreendimento.gpkg)

Polígono didático do empreendimento fictício usado ao longo do curso:

- **Nome:** Parque Solar Cerrado Vivo
- **Tipologia:** Usina Solar Fotovoltaica (empreendimento fictício)
- **Localização:** Planaltina-GO, região do Cerrado goiano
- **Área:** ~220 ha
- **Formato:** GeoPackage (GPKG) — SIRGAS 2000, EPSG:4326

> Este polígono foi posicionado em uma área do Cerrado com características ambientais representativas: APA do Planalto Central na área de influência, histórico de desmatamento PRODES, vegetação nativa predominante (~96%) e pressão de fogo documentada. Ideal para demonstrar todas as verificações do pipeline.

### Módulos 02 a 06

Estes módulos não requerem arquivos adicionais — todos os dados são consultados diretamente via APIs públicas dentro dos notebooks.

---

## Tecnologias e fontes de dados

**Linguagem:** Python 3 · **Ambiente:** Google Colab

**Bibliotecas principais:**
`geopandas` · `rasterio` · `shapely` · `requests` · `matplotlib` · `contextily`

**Fontes de dados (todas públicas e gratuitas):**

| Dado | Fonte | Acesso |
|---|---|---|
| Unidades de Conservação | ICMBio / TerraBrasilis | WFS aberto |
| Terras Indígenas | FUNAI / TerraBrasilis | WFS aberto |
| Hidrografia federal | ANA / TerraBrasilis | WFS aberto |
| Uso e cobertura 30m (1985–2024) | MapBiomas Col. 10 | AWS S3 público |
| Uso e cobertura 10m (2019–2024) | MapBiomas Col. 2 | Google Cloud público |
| Desmatamento PRODES | INPE / TerraBrasilis | WFS aberto |
| Alertas DETER | INPE / TerraBrasilis | WFS aberto |
| Focos de fogo | NASA FIRMS + INPE | CSV público |
| Limites administrativos | IBGE | API pública |

---

## Sobre o professor

**Hugo José Ribeiro**  
Professor e pesquisador na Escola de Engenharia Civil e Ambiental da Universidade Federal de Goiás (EECA/UFG).

Trabalha com ciência de dados ambientais, sensoriamento remoto, GeoAI e análise espacial aplicados a problemas ambientais e urbanos no Brasil.

🔗 [github.com/hgribeirogeo](https://github.com/hgribeirogeo)  
🔗 [Currículo Lattes](http://lattes.cnpq.br/9999213878472864)

---

## Licença

Os arquivos de dados disponibilizados neste repositório são de uso livre para fins educacionais.  
Os notebooks e materiais didáticos do curso são de uso exclusivo dos matriculados.

---

*Curso de Extensão — UFG/EECA · Automação Geoespacial para Licenciamento Ambiental*
