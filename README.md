# 🎧 Spotify ETL Pipeline - Artistas Específicos

![Python](https://img.shields.io/badge/Python-3.12-blue.svg)
![Google Colab](https://img.shields.io/badge/Google%20Colab-Notebook-orange)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-green)
![Spotipy](https://img.shields.io/badge/Spotify%20API-Spotipy-lightgreen)
![License](https://img.shields.io/badge/license-MIT-lightgrey)

> Pipeline de ETL em Python/Colab que consome a API do Spotify para coletar faixas de **artistas específicos**, transforma com Pandas e exporta em **CSV** e **Parquet**, além de gerar visualizações simples.

---

## 📘 Sumário
1. [📋 Objetivo](#-objetivo)  
2. [🧠 O que o projeto faz](#-o-que-o-projeto-faz)  
3. [🧩 Tecnologias utilizadas](#-tecnologias-utilizadas)  
4. [🚀 Como testar o projeto](#-como-testar-o-projeto)  
5. [📊 Resultados esperados](#-resultados-esperados)  
6. [💡 Próximos passos](#-próximos-passos)  
7. [👨‍💻 Autor](#-autor)  
8. [⚖️ Licença](#️-licença)

---

## 📋 Objetivo
Este projeto implementa um **pipeline completo de Engenharia de Dados** com a **API pública do Spotify**, usando Python e Google Colab.  
Ele demonstra como criar um fluxo de **extração, transformação e carga (ETL)** em dados musicais, focando em **artistas específicos** em vez de playlists.  
Ideal para quem quer aprender a integrar APIs, tratar dados com Pandas e exportar resultados em múltiplos formatos.

---

## 🧠 O que o projeto faz

1. **Autenticação**  
   - Conecta-se à API do Spotify via `SpotifyClientCredentials` usando chaves seguras do Colab (`userdata`).

2. **Extração de dados**
   - Coleta até 10 faixas por artista definido na lista do notebook.
   - Armazena nome da faixa, artista, álbum, data de lançamento e popularidade.

3. **Transformação**
   - Organiza os dados em um `DataFrame` Pandas.
   - Realiza limpeza e estruturação.

4. **Carga**
   - Salva o resultado final em:
     - `spotify_tracks_artists.csv`
     - `spotify_tracks_artists.parquet`

5. **Visualização**
   - Exibe gráficos com:
     - Popularidade média por artista.
     - Distribuições simples para análise exploratória.

---

## 🧩 Tecnologias utilizadas
- Python 🐍  
- Spotipy 🎧 (integração com Spotify API)  
- Pandas 🧮  
- Matplotlib 📊  
- Google Colab ☁️  

---

## 🚀 Como testar o projeto

1. **Abra o notebook no Google Colab**  
   Suba o arquivo `spotify_etl_artists_pipeline.ipynb` para o seu repositório e abra no Colab ou use o link de abertura direta do seu GitHub.

2. **Adicione suas chaves da API do Spotify**
   - Acesse o [Spotify Developer Dashboard](https://developer.spotify.com/dashboard)  
   - Crie um app e copie:
     - `Client ID`
     - `Client Secret`
   - No Colab, adicione como segredos:  
     **Configurações → Gerenciar segredos →**  
     `SPOTIPY_CLIENT_ID` = *seu client id*  
     `SPOTIPY_CLIENT_SECRET` = *seu client secret*

3. **Execute todas as células**
   - A execução completa costuma levar ~30–60 segundos.
   - Os arquivos finais são gerados em `/content/` (ou no seu Drive, se você tiver configurado).

---

## 📊 Resultados esperados
- Arquivo **CSV** e **Parquet** com informações das faixas.  
- Gráfico de barras mostrando a **popularidade média por artista**.

---

## 💡 Próximos passos
- Introduzir a coleta de *audio features* (dançabilidade, energia, valência, etc.) com fallback.  
- Integrar com **Apache Spark** para maior escala.  
- Publicar painéis interativos com **Streamlit**/**Dash**.  
- Criar um workflow de **CI** (GitHub Actions) para validação rápida (smoke tests).

---

## 👨‍💻 Autor
**Uilian Nunes**  
Tech Lead  
[LinkedIn](https://linkedin.com/in/uiliannunes) • [GitHub](https://github.com/uiliannunes)

---

## ⚖️ Licença
Este projeto está licenciado sob os termos da **MIT License**.  
Você é livre para usar, copiar, modificar e distribuir este software, desde que mantenha o aviso de copyright e a licença original.
