# Metaverso Lapa · Grupo Vandic Rocha

Experiência 3D no navegador com a Lapa e a Glória, no Rio de Janeiro, e a sede virtual do Grupo Vandic Rocha.

## Locais

| Local | O que tem |
| --- | --- |
| Arcos da Lapa | 42 arcos em dois níveis (270 m, 17,6 m) e o bonde de Santa Teresa passando por cima |
| Escadaria Selarón | Degraus e muretas de azulejo, com subida até Santa Teresa |
| Passeio Público | Portão de 1783, Chafariz dos Jacarés, pirâmides de Mestre Valentim, palmeiras imperiais |
| Feira da Glória | 16 barracas (hortifruti, flores, peixaria, pastel e caldo de cana…) |
| Torre Vandic Rocha | Andares da Setfrio e da Petrorio, condensadoras VRF na cobertura |
| Escritório Lapa Coin | Cobertura com as 10 moedas do grupo girando em volta do núcleo; ao tocar numa moeda aparece o contrato BEP-20 |

## Tecnologia

- Three.js r169 (WebGL) carregado de CDN por import map, sem build
- Materiais PBR com iluminação de ambiente (PMREM + RoomEnvironment), tone mapping ACES Filmic
- Pós-processamento com bloom (UnrealBloomPass) para a iluminação noturna
- Sombras suaves (PCF), instancing para arcos, degraus, árvores, gradil e frutas
- Texturas procedurais em canvas: azulejos Selarón, pedra portuguesa em ondas, fachadas coloniais
- Modo dia/noite, minimapa, joystick de toque no celular e WebXR (botão VR aparece em óculos compatíveis)

## Como abrir

Os arquivos precisam ser servidos por HTTP (módulos ES):

```sh
cd media/metaverso
python3 -m http.server 8080
# abra http://localhost:8080
```

Controles: `W A S D` ou setas para andar, `Shift` para correr, arrastar para girar a câmera, roda do mouse para zoom.
No celular, use o joystick da esquerda e arraste a tela para olhar. O círculo dourado na entrada da torre sobe para a cobertura.

## Tokens (BNB Smart Chain)

Os logos em `tokens/` são cópias dos arquivos em `blockchains/smartchain/assets/<contrato>/logo.png`.

| Símbolo | Nome | Contrato |
| --- | --- | --- |
| LAPA | Lapa Coin | `0xC12e14135b82305637e4F3c2FE4eaB7739854D10` |
| SET | Moeda Setfrio | `0x6779eF4dE8343Dd8DA82158410D3934F68603f65` |
| PTR | Moeda Petrorio | `0xB9dFF02ba6d2BE0a3A49382f983D87ddaAd804B4` |
| PTF | Moeda Petrorio PTF | `0xD0Af1bD51ee0132858A172D41eC769e1e3Cf9c11` |
| PET | Pet Resgate | `0x544510c97944b0579B27c4a7FBB76412b1336601` |
| HVAC-R | Moeda HVAC-R | `0x4c3d87d7faaf04e17c9de0afbce4687aa7793995` |
| AVAC-R | AVAC-R 2026 | `0x935CbCb59719dAC5DDc72c6d9e11b95f18834876` |
| AVAC | AVAC-R Coin Inc. | `0x2fe3c7dd588a1258f032a776e33266aed46256f0` |
| GCC | Green Cooling Credit | `0x83Df478CB43c95dAab29259A6c308C157D62a2E7` |
| VGI | Vandic Global Index | `0xd78342A74D251891d9Daa6D709fC3bab5803c78A` |

O contrato `0xB9dF…04B4` foi adicionado no commit "Add PET token logo", mas o logo mostra "PTR · Moeda Petrorio", então aqui ele aparece como PTR.
