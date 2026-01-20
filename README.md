# – Plataforma de Ensino Tech

Este projeto consiste no desenvolvimento do Front-End de **uma plataforma de ensino tech** focada em tecnologia.  
O objetivo foi criar uma interface **moderna, responsiva e funcional**, utilizando apenas **HTML5 e CSS3** e **Bootstrap 5**, **sem qualquer uso de JavaScript**, 
para reforçar o aprendizado com essas tecnologias.


## 📜 Instruções para desenvolvimento


[Instruções seguidas para o desenvolvimento do projeto](https://github.com/L0pe5/ProjetoBootstrap)


---

## 🧑‍💻 Tecnologias

O projeto é foi desenvolvido utilizando as seguintes tecnologias:

 ![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white) ![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white) ![Bootstrap](https://img.shields.io/badge/Bootstrap-563D7C?style=flat&logo=bootstrap&logoColor=white)

---
## 📂 Estrutura do Projeto

O projeto é composto por três arquivos principais:

- **index.html** → Landing Page institucional  
- **dashboard.html** → Área logada do aluno (Painel de Controle)  
- **style.css** → Estilização geral, variáveis de tema e lógicas de interação  

---

## 📄 Detalhamento das Páginas

### 1. `index.html` – Landing Page

Página com foco total em **conversão de visitantes em alunos**.

#### 🔹 Componentes:
- **Navbar**  
  Barra de navegação fixa com links de âncora e botão **Entrar**, que aciona um modal.

- **Hero Section**  
  Apresentação principal com vídeo em loop e chamadas para ação (CTAs).

- **Trilhas (Carrossel)**  
  Exibição dos cursos disponíveis.  
  🔥 Destaque: carrossel funcional feito com **Radio Buttons + CSS puro** (zero JavaScript).

- **Agenda**  
  Tabela estilizada (`.table-dark`) listando eventos, workshops e mentorias.

- **Pricing (Planos)**  
  Comparativo com três planos (**Free**, **Plus**, **Enterprise**), com destaque visual para o plano **Plus**.

- **Comunidade**  
  Cards com estatísticas da plataforma usando **Bootstrap Icons**.

- **Footer & Contato**  
  Rodapé com links sociais e formulário de contato visual.

- **Modais**  
  Dois modais (**Login/Cadastro** e **Feedback**) controlados via **Checkbox Hack**.

---

### 2. `dashboard.html` – Área do Aluno

Página focada na **experiência de aprendizado e acompanhamento de progresso**.

#### 🔹 Estrutura:
- **Layout Grid**  
  CSS Grid dividindo a tela em:  
  `Header | Sidebar | Main | Widgets`

- **Navbar Logada**  
  Campo de busca responsivo, notificações e menu de perfil  
  (Dropdown ativado via `:hover`).

- **Sidebar**  
  Menu de navegação lateral.  
  No mobile, funciona como **Off-canvas**, deslizando da lateral.

#### 🔹 Conteúdo Principal:
- Boas-vindas personalizadas  
- **Cursos em Progresso** com barras de progresso reais  
- **Carrossel Plus** exclusivo para assinantes  
- **Eventos e Agenda** em visualização rápida  

#### 🔹 Widgets Laterais:
- Gráfico de metas semanais  
- Atalho para a comunidade no Discord  

---

## 🎨 Bootstrap 5 – Classes Utilizadas

Framework Bootstrap utilizado para acelerar a estruturação do layout e a estilização base, colocando em prática o conhecimento adquirido durante o curso.

### 📐 Grid System
- `container`, `container-fluid`
- `row`
- `col-12`, `col-md-6`, `col-lg-3`, `col-lg-auto`

### 📦 Flexbox Utilities
- `d-flex`, `flex-column`, `flex-wrap`
- `justify-content-center`, `justify-content-between`
- `align-items-center`
- `gap-3`

### 📏 Espaçamento e Tamanho
- `m-5`, `p-4`, `py-3`
- `w-100`, `h-100`
- `mb-4`

### 🧩 Componentes
- `navbar`, `navbar-expand-lg`
- `card`, `card-body`, `card-img-top`
- `btn`, `btn-primary`, `btn-outline-light`
- `badge`, `rounded-pill`
- `progress`, `progress-bar`
- `alert`
- `form-control`, `form-select`, `form-check`
- `table`, `table-hover`

### 👁️ Visibilidade
- `d-none`, `d-lg-block`, `d-lg-none`

### 🔤 Tipografia
- `fw-bold`, `text-uppercase`, `text-muted`
- `display-4`, `fs-4`

---

## 🛠️ CSS Personalizado – Onde e Por Quê?

O uso do **CSS (`style.css`)** foi essencial para customização em três pilares:

- Lógica *CSS-only* (sem JavaScript)
- Responsividade do layout em diferentes dispositivos
- Identidade visual (tema dark) 


### 🎨 Identidade Visual (Dark Theme)
- Criação de variáveis CSS (`:root`) com tons de azul profundo  
  (`#000814`, `#001D3D`)
- Sobrescrita das cores padrão do Bootstrap
- Uso de `background-image` com **gradientes lineares**
- Uso de animações/transições simples com `@keyframes` e `transition` para efeitos sutis
- Customização de botões, cards e tabelas para manter coerência visual
- Personalização de formulários para melhor usabilidade no tema dark
- Estilização de modais para integração visual com o restante da página
- Responsividade aprimorada com media queries específicas


---

### 🧠 Lógica *CSS-only* (Sem JavaScript)

Como JS era proibido, a solução foi utilizar as ferramentas disponíveis noCSS:

#### ✔ Checkbox Hack
- Inputs `checkbox` invisíveis (`display: none`)
- Controle de estado via seletor de irmãos (`~`)

**Exemplos de uso:**
- Sidebar mobile:  
  `#sidebar-toggle:checked ~ .dashboard-grid .dash-sidebar`
- Modais:  
  `#modal-toggle:checked ~ .modal-overlay`
- Carrossel CSS:  
  Uso de `radio buttons` + `transform: translateX()`

---

### 🧱 Layout Avançado
- **CSS Grid no Dashboard**  
  Ideal para layout 2D com sidebar fixa e conteúdo rolável.
- **Efeitos Visuais Customizados**
  - `.glowing-border` → efeito neon
  - `.bg-overlay` → efeito vidro
- **Scrollbar Personalizada**
  - Customização de `::-webkit-scrollbar` para manter coerência com o tema dark

---

## ⚠️ Principais Dificuldades e Soluções

### 🔄 Interatividade sem JavaScript
**Problema:** Criar modais e carrossel funcionais  
**Solução:** Uso do **Checkbox Hack**, com labels corretamente vinculados aos inputs invisíveis `d-none`.

---

### 📐 Conflito de Layout na Navbar (Dashboard)
**Problema:** Quebra indesejada da busca e ícones em tablets  
**Solução:**  
- `w-100` no mobile  
- `w-50` + `flex-wrap` no desktop  

---

### ⬇️ Dropdown do Bootstrap
**Problema:** Dropdown depende do Popper.js  
**Solução CSS:**
```css
.dropdown:hover .dropdown-menu {
  display: block;
}
