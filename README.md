# 🚀 JP Language

Uma linguagem de programação moderna que compila para C++ com sistema de módulos nativos.

## ⚡ Instalação Rápida

1. **Baixe** o `jp.exe` da [página de releases](https://github.com/Joaopaulopadilha/jp-language/releases)
2. **Copie** para uma pasta no seu PATH (ex: `C:\Windows\System32\`)
3. **Teste**: abra cmd/PowerShell e digite `jp version`

## 🎯 Primeiro Programa

Crie um arquivo `hello.jp`:
```javascript
print("Olá, mundo!")

nome = input("Seu nome: ")
print("Olá,", nome, "!")
```

Execute:
```bash
jp run hello.jp
```

## 🪟 Exemplo com Janela Nativa

```javascript
// window_demo.jp
import window

print("Criando janela...")
win = createWindow("Meu App JP", 800, 600)

print("Janela criada! Pressione ESC para fechar.")
while pollEvents(win) {
    if isKeyPressed(VK_ESCAPE) {
        print("ESC pressionado - fechando...")
        break
    }
}

destroyWindow(win)
print("Janela fechada!")
```

Execute:
```bash
jp install window    # Instala módulo de janelas
jp run window_demo.jp
```

## 📦 Sistema de Módulos

```bash
# Package manager integrado
jp install window     # Janelas nativas
jp install math       # Funções matemáticas  
jp install random     # Números aleatórios
jp list               # Lista módulos instalados
jp info window        # Informações do módulo
```

## 📚 Comandos Disponíveis

| Comando | Descrição | Exemplo |
|---------|-----------|---------|
| `jp run arquivo.jp` | Compila e executa | `jp run game.jp` |
| `jp compile arquivo.jp` | Só compila para C++ | `jp compile lib.jp` |
| `jp install modulo` | Instala módulo | `jp install math` |
| `jp list` | Lista módulos | `jp list` |
| `jp remove modulo` | Remove módulo | `jp remove math` |
| `jp info modulo` | Info do módulo | `jp info window` |
| `jp version` | Versão do JP | `jp version` |
| `jp help` | Ajuda completa | `jp help` |

## 🔧 Sintaxe da Linguagem

### Variáveis
```javascript
nome = "João"           // String
idade = 25              // Integer  
altura = 1.75           // Float
ativo = true            // Boolean

// Tipagem explícita
int contador = 0
string titulo = "App"
```

### Funções
```javascript
int somar(int a, int b) {
    return a + b
}

resultado = somar(10, 20)
print("Resultado:", resultado)
```

### Controle de Fluxo
```javascript
// Condicionais
if idade >= 18 {
    print("Maior de idade")
} else {
    print("Menor de idade")
}

// Loops
for i in range(10) {
    print("Número:", i)
}

while ativo {
    // código aqui
}

repeat 5 {
    print("Repetindo...")
}
```

### Módulos
```javascript
// Importa módulo completo
import math
resultado = sqrt(16)

// Importa função específica  
from window import createWindow
janela = createWindow("App", 640, 480)
```

## 🎮 Exemplos Práticos

### Calculadora
```javascript
// calc.jp
import math

print("=== Calculadora JP ===")
a = input("Primeiro número: ")
b = input("Segundo número: ")

print("Soma:", a + b)
print("Raiz de", a, "=", sqrt(a))
```

### Jogo Simple
```javascript
// game.jp  
import window
import random

win = createWindow("Snake Game", 800, 600)
score = 0

while pollEvents(win) {
    if isKeyPressed(VK_SPACE) {
        score = score + 1
        print("Score:", score)
    }
    
    if isKeyPressed(VK_ESCAPE) {
        break
    }
}

print("Game Over! Score final:", score)
```

## 🌍 Plataformas Suportadas

- ✅ **Windows** 10/11 (x64)
- ⏳ **Linux** (em breve)
- ⏳ **macOS** (em breve)

## 📄 Licença

MIT License - use livremente!

## 👤 Autor

**João Paulo Padilha**
- GitHub: [@Joaopaulopadilha](https://github.com/Joaopaulopadilha)

---

**JP Language - Programação simples que compila para C++** 🚀

### 📥 [Download jp.exe](https://github.com/Joaopaulopadilha/jp-language/releases/latest)
