# Mapa de exposição ao calor – trabalho a céu aberto (Curitiba)

Mapa interativo do **WBGT** (índice de bulbo úmido–termômetro de globo) para orientar a proteção de trabalhadores
externos em Curitiba: onde e quando a exposição ao calor é maior, considerando sol, sombra de edifícios e árvores,
temperatura das superfícies e condições meteorológicas.

- **Cenários**: dia médio e dia quente (P90) nas quatro estações do ano, das 9 h às 17 h.
- **Tempo real**: WBGT nas estações meteorológicas de Curitiba, atualizado a cada 20 minutos, e as condições do momento
  aplicadas a cada pixel de 30 m.
- **Classes** em faixas de 1 °C ancoradas no P98 histórico do WBGT máximo diário de Curitiba em campo aberto (27,1 °C;
  INMET A807, 2003–2025).

## Estrutura do repositório
| Caminho | Conteúdo |
|---|---|
| `docs/index.html` | o mapa (arquivo único, abre em qualquer navegador) |
| `render.yaml` | configuração do site estático no Render (publica a pasta `docs`) |
| branch `tempo-real` → `tempo_real.json` | dados em tempo real, regravados a cada 20 min pelo CISC |

## Fontes
Landsat 8/9 (temperatura de superfície), Google Open Buildings 2.5D (altura dos edifícios), Meta/WRI Global Canopy
Height (copa das árvores), estações meteorológicas automáticas de Curitiba (CISC), Open-Meteo (dados ausentes) e
INMET A807 (limiar). Método: Tmrt (SOLWEIG / VDI 3787) e WBGT (ISO 7243/7726).

Centro de Inteligência em Saúde e Clima (CISC) – Secretaria Municipal da Saúde de Curitiba.
