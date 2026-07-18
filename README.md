# PMG Play — Digital Twin Jogável

Build **WebGL** do digital twin do galpão industrial (107 × 30 m) — a versão jogável do projeto Unity `industry fundamentals`, publicada no **Vercel**.

Versão só-visualização (viewer Three.js leve): https://jpeixer.github.io/digital-twin-galpao/

## Como jogar

| Tecla | Modo AGV (3ª pessoa) | Modo Drone |
|---|---|---|
| **W/S** | acelera / ré | drone avança / recua |
| **A/D** | vira | drone desliza lateral |
| **← →** | orbita a câmera | gira a vista |
| **↑ ↓** | eleva/abaixa a câmera | inclina a vista |
| **V** | ativa o drone | volta ao AGV |
| **F1** | painel do céu dinâmico (hora, velocidade do tempo, clima) | idem |

Dirija o AGV pelo pátio e entre na fábrica pelos portões abertos (hall → Testing Lab → packaging).

## Stack

- Unity 6 (URP) — cena `teste.unity`
- Céu dinâmico: motor do **Tenkoku** (sol/tempo) em modo híbrido URP + skybox procedural
- Terrain do demo Tenkoku reposicionado; prédio conforme projeto arquitetônico PFIFFNER/MOSER GLASER
- Build WebGL com Brotli + decompression fallback (não precisa de headers especiais)

## Atualizar o build

1. Unity: **File → Build Settings → WebGL → Build** para `Builds/WebGL`
2. Copiar o conteúdo para este repositório (substituindo `index.html`, `Build/`, `TemplateData/`)
3. `git commit` + `git push` — o Vercel publica sozinho
