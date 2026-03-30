# 🐾 Pou — Mascote Virtual

Um jogo completo de mascote virtual (tamagotchi digital) feito inteiramente em **HTML, CSS e JavaScript puro**, em um único arquivo. Sem frameworks, sem dependências, sem build — basta abrir no navegador e jogar.

> Cuide do Pou: alimente, brinque, dê banho e coloque para dormir. Mantenha seus atributos em dia e suba de nível!

---

## 🎮 Jogar

1. Faça o download ou clone este repositório.
2. Abra o arquivo `pou.html` em qualquer navegador moderno.
3. Pronto — funciona 100% offline.

```bash
git clone https://github.com/seu-usuario/pou-virtual-pet.git
cd pou-virtual-pet
open pou.html   # macOS
# ou: start pou.html (Windows) / xdg-open pou.html (Linux)
```

---

## ✨ Funcionalidades

### Atributos e Status

| Atributo     | Ícone | Decaimento          | Efeito quando baixo                          |
|:-------------|:-----:|:---------------------|:----------------------------------------------|
| Fome         | 🍔    | −1 a cada 30s       | Expressão triste; abaixo de 0% fica doente   |
| Felicidade   | ⭐    | −1 a cada 45s       | Pou chora com lágrimas animadas              |
| Higiene      | 🚿    | −1 a cada 60s       | Nuvens de mau cheiro; Pou fica esverdeado    |
| Energia      | ⚡    | −1 a cada 50s       | Olhos sonolentos; dorme automaticamente em 0% |

### Alimentação

9 alimentos disponíveis com diferentes valores de fome, felicidade e preço — de uma simples maçã (🍎 2 moedas) até sushi premium (🍣 15 moedas). Inclui vitamina (💊) que cura doenças.

### 3 Minijogos

- **🧩 Quebra-Cabeça de Cores** — Elimine grupos de blocos da mesma cor em um grid 4×4.
- **⭐ Pegar Estrelas** — Clique nas estrelas que caem antes que desapareçam (30 segundos).
- **🎨 Sequência de Cores** — Memorize e repita a sequência mostrada (estilo Simon).

Cada minijogo recompensa com felicidade, XP e moedas.

### Sistema de Banho

Modo interativo onde você esfrega a esponja no Pou com o mouse/toque. Bolhas de sabão animadas sobem enquanto o progresso de limpeza aumenta.

### Sistema de Sono

Fundo de noite estrelada com animação de "Zzz" flutuantes. A energia recupera +10 a cada 5 segundos até chegar a 100%.

### Loja

| Categoria     | Itens                                                   |
|:--------------|:--------------------------------------------------------|
| 🎩 Chapéus    | Boné, Coroa, Chapéu de Bruxa, Capacete de Astronauta   |
| 🖼️ Fundos     | Praia Tropical, Floresta Mágica, Espaço Sideral, Neon  |
| ⚡ Poderes    | Dobro de XP, Regeneração de Fome, Super Feliz           |

Itens são desbloqueados conforme o nível do Pou.

### Progressão

- **XP e Nível** — Ganhe XP alimentando, brincando e dando banho. Máximo: nível 50.
- **Moedas** — Ganhas nos minijogos, usadas para comprar alimentos e itens na loja.
- **Crescimento** — O Pou cresce visualmente a cada nível.

---

## 🔧 Detalhes Técnicos

| Item                | Detalhe                                        |
|:--------------------|:-----------------------------------------------|
| Arquivo             | Um único `pou.html`                            |
| Linguagem           | HTML5 + CSS3 + JavaScript (ES6+)               |
| Frameworks          | Nenhum — Vanilla JS puro                       |
| Gráficos do Pou     | SVG inline (sem imagens externas)              |
| Áudio               | Web Audio API (sons sintetizados, sem arquivos) |
| Persistência        | `localStorage` com save automático a cada 30s  |
| Cálculo offline     | Desconta atributos proporcionais ao tempo ausente (máx. 8h) |
| Responsividade      | Layout 540×960px centralizado, touch-friendly  |

### Arquitetura do Código

O código está organizado em módulos lógicos separados por responsabilidade:

- **`GS`** — Estado global do jogo (GameState)
- **`Storage`** — Salvar/carregar dados no localStorage
- **`Audio`** — Síntese de sons com Web Audio API
- **`UI`** — Renderização, barras, efeitos visuais e partículas
- **`Feed`** — Sistema de alimentação
- **`MiniGames`** — Os 3 minijogos
- **`Bath`** — Sistema de banho interativo
- **`Sleep`** — Sistema de sono e recuperação
- **`Shop`** — Loja com categorias e equipamento

---

## 🎨 Animações

O Pou possui diversas animações e expressões que respondem ao seu estado:

- Respiração suave em idle (escala cíclica)
- Piscada automática a cada 3–5 segundos
- Sorriso quando feliz, boca triste quando com fome
- Lágrimas animadas quando infeliz
- Olhos semicerrados quando sonolento
- Nuvens de mau cheiro quando sujo
- Cor esverdeada quando muito sujo
- Balanço lateral quando triste/doente
- Partículas coloridas ao alimentar
- Confete ao completar minijogos
- Texto "LEVEL UP!" com explosão de estrelas

---

## 📱 Compatibilidade

- ✅ Chrome / Edge / Brave
- ✅ Firefox
- ✅ Safari (desktop e iOS)
- ✅ Dispositivos móveis (touch events)
- ✅ Funciona offline (sem requisições de rede)

---

## 📄 Licença

Este projeto é de código aberto. Sinta-se livre para usar, modificar e distribuir.

---

<p align="center">
  Feito com ❤️ em um único arquivo HTML
</p>
