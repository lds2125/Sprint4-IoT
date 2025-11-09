# 🏍️ Monitoramento de Motos com Visão Computacional

Este projeto demonstra um **fluxo completo de dados** com **visão computacional simulada**, desde a **captura** (detecção de motos via câmera) até a **visualização final** em um **dashboard interativo no Google Colab**.  

O objetivo é monitorar o **pátio de motos** em tempo real, identificando:
- A **localização** de cada moto (em um mapa tipo grid);
- O **estado operacional** (em uso, parada, manutenção);
  
---

## 🚀 Tecnologias Utilizadas

| Tecnologia | Finalidade |
|-------------|-------------|
| **Python 3.x** | Linguagem principal |
| **Google Colab** | Execução e visualização online |
| **Pandas** | Manipulação de dados |
| **NumPy** | Normalização e cálculos matriciais |
| **Matplotlib** | Criação do dashboard / mapa visual |
| **Datetime / Random** | Geração de dados simulados e timestamps |

---

## ⚙️ Estrutura do Projeto

📂 projeto-monitoramento-motos/
├── patio_visao_computacional.ipynb # Notebook completo (Colab)
├── README.md # Este arquivo


---

## 💻 Como Executar no Google Colab

### 1️⃣ Abrir diretamente no Colab

1. Faça login no [Google Colab](https://colab.research.google.com/).  
2. Vá em **Arquivo > Enviar notebook** e envie o arquivo  
   `patio_visao_computacional.ipynb`.  
3. Execute.

---

## 📊 Resultados Finais

O notebook gera automaticamente:

### 🗺️ **Mapa do Pátio**
Visualização em grid representando a posição de cada moto.  
As cores indicam o estado:
- 🟩 **Verde** – em uso  
- 🟦 **Azul** – parada  
- 🟥 **Vermelho** – manutenção  

---

## 🧠 Lógica do Sistema

1. **Captura (Simulada)** – `detectar_motos_frame()` gera detecções com `bbox` e `confidence`.  
2. **Mapeamento** – O centro do `bbox` é convertido para posições em um grid do pátio.  
3. **Estado da Moto** – Cada moto recebe um estado aleatório (`em_uso`, `parada`, `manutencao`).   
4. **Dashboard** – O pátio é renderizado em um mapa colorido usando `matplotlib`.
