# Validação HTML com Regex

## 📋 Descrição

Este projeto é uma **demonstração interativa** de validação de formulários HTML utilizando **expressões regulares (regex)** através do atributo `pattern`.  
A aplicação permite testar diferentes padrões de validação para campos comuns como **CPF, telefone, e-mail**, entre outros.

**Destaque:** Implementação de um **tema dark moderno** com validação visual inteligente que não mostra erros em campos vazios.

---

## ✨ Funcionalidades

- ✅ **Validação em tempo real** usando o atributo `pattern` do HTML5  
- 🎯 **Feedback visual inteligente** - campos vazios não mostram erro
- 💡 **Explicação das expressões regulares** utilizadas  
- 📱 **Design responsivo** para diferentes tamanhos de tela  
- 🎨 **Tema dark moderno** com paleta de cores harmoniosa
- 🌙 **Interface escura** que reduz a fadiga visual

---

## 🛠️ Tecnologias Utilizadas

| Tecnologia | Descrição |
|-------------|------------|
| **HTML5** | Estrutura da página e elementos de formulário |
| **CSS3** | Tema dark e design responsivo |
| **JavaScript** | Interatividade básica |
| **Regex** | Validação de padrões nos campos |
| **CSS Variables** | Sistema de cores consistente para o tema dark |

---

## 🎨 Sistema de Cores do Tema Dark

| Variável CSS | Cor | Uso |
|-------------|------|-----|
| `--dark-bg` | `#111827` | Cor de fundo principal |
| `--dark-text` | `#9494a5` | Texto principal |
| `--dark-secondary-text` | `#9ca3af` | Texto secundário |
| `--dark-card-bg` | `#1f2937` | Fundo dos cards/containers |
| `--dark-border` | `#374151` | Bordas dos elementos |
| `--dark-drag-hover` | `#293548` | Estados de hover |

---

## ⚡ Solução CSS para Validação de Campos Vazios

O projeto implementa uma **solução puramente CSS** para evitar que campos vazios mostrem erro:

```css
/* Apenas mostra validação quando NÃO está vazio */
input:not(:placeholder-shown):valid {
    border-color: #34d399; /* Verde para válido */
}

input:not(:placeholder-shown):invalid {
    border-color: #f87171; /* Vermelho para inválido */
}
```

**Como funciona:**
- `:placeholder-shown` - Detecta quando o placeholder está visível (input vazio)
- `:not(:placeholder-shown)` - Seleciona apenas inputs preenchidos
- Combinação com `:valid`/`:invalid` - Aplica validação apenas quando relevante

**Resultado:**
- ✅ **Campos vazios**: Borda padrão (cinza)
- ✅ **Campos preenchidos e válidos**: Borda verde
- ✅ **Campos preenchidos e inválidos**: Borda vermelha

---

## 📝 Campos de Validação

| Campo | Regex | Descrição |
|-------|--------|-----------|
| **PIN** | `[0-9]{4}` | Exatamente 4 dígitos numéricos |
| **Nome** | `[A-Za-zÀ-ÿ]{3,}` | Mínimo 3 letras (incluindo acentos) |
| **E-mail** | `[a-z0-9._%+-]+@[a-z0-9.-]+\.[a-z]{2,}$` | Formato de e-mail padrão |
| **Telefone BR** | `(\([0-9]{2}\)\s?)?[0-9]{4,5}-?[0-9]{4}` | Telefone brasileiro com ou sem DDD |
| **CPF** | `[0-9]{3}\.?[0-9]{3}\.?[0-9]{3}-?[0-9]{2}` | CPF brasileiro (com ou sem pontuação) |
| **Senha** | `^(?=.*[A-Z])(?=.*\d).{8,}$` | Mínimo 8 caracteres, 1 letra maiúscula e 1 número |
| **Data** | `(0[1-9]\|[12][0-9]\|3[01])/(0[1-9]\|1[0-2])/[0-9]{4}` | Formato **DD/MM/AAAA** |
| **CEP** | `[0-9]{5}-?[0-9]{3}` | CEP brasileiro (com ou sem hífen) |

---

## 🚀 Como Usar

1. **Clone ou baixe** o arquivo HTML
   ```bash
   git clone https://github.com/valdir-alves3000/html-regex-validation.git
   ```

2. **Abra o arquivo** `index.html` em qualquer navegador moderno

3. **Preencha os campos** do formulário e observe a validação inteligente

4. **Teste diferentes cenários**:
   - Campos vazios (sem validação visual)
   - Campos preenchidos corretamente (borda verde)
   - Campos preenchidos incorretamente (borda vermelha)

5. **Envie o formulário** apenas quando todos os campos estiverem válidos

---

## 🌐 Compatibilidade

### Navegadores Suportados:
- **Chrome 10+** ✅
- **Firefox 4+** ✅  
- **Safari 10.1+** ✅
- **Edge 12+** ✅
- **Internet Explorer 10+** ✅

### Suporte CSS Avançado:
- **`:placeholder-shown`**: Chrome 47+, Firefox 51+, Safari 9+, Edge 79+
- **CSS Variables**: Todos os navegadores modernos

---

## 📱 Responsividade

O layout se adapta automaticamente para diferentes dispositivos:

- **🖥️ Desktop**: Layout em duas colunas
- **📱 Tablet**: Layout adaptativo
- **📱 Mobile**: Layout em uma única coluna

---

## 🔧 Personalização

### Para modificar as expressões regulares:
1. Localize o campo desejado no HTML
2. Altere o valor do atributo `pattern`
3. Atualize o texto do atributo `title` para refletir a nova validação
4. Edite a explicação na div `.regex-info`

### Para personalizar o tema dark:
1. Modifique as variáveis CSS no `:root`
2. Ajuste as cores conforme necessário
3. Mantenha a consistência da paleta

---

## 💡 Casos de Uso

- **Aprendizado** de expressões regulares
- **Demonstração** de validação HTML5
- **Prototipagem rápida** de formulários
- **Referência** para implementação de temas dark
- **Estudo** de técnicas CSS avançadas

---

**🚀 Desenvolvido para demonstrar o poder da validação HTML5 com Regex e implementação de temas dark modernos!**
