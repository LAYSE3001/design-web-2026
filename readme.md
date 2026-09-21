# Tarefa 33: Página pessoal com DaisyUI
Tarefa 33: Minha página pessoal com DaisyUI

Nesta tarefa eu montei uma página pessoal de apresentação usando os componentes do DaisyUI junto com o Tailwind. A página está no arquivo tarefa33.html e tem quatro seções: cabeçalho, sobre mim, projetos e contato.

Para ver a página, é só abrir o tarefa33.html no navegador.

1. Componentes DaisyUI utilizados
Componente	Onde aparece na página
navbar	Topo da página, com meu nome, os links de navegação, o botão de tema e o botão "Fale comigo"
menu (menu-horizontal)	Links Sobre, Projetos e Contato dentro da navbar
hero	Logo abaixo da navbar, com o título, uma frase de apresentação e dois botões
btn (btn-primary, btn-outline, btn-ghost)	Navbar, hero, cards e formulário. O btn-primary está em "Fale comigo", "Ver projetos" e "Enviar mensagem". O btn-outline está em "Saber mais" e nos botões de dois cards. O btn-ghost é o meu nome na navbar
badge (badge-primary, badge-secondary, badge-accent, badge-outline)	Seção "Sobre mim", destacando as tecnologias e áreas que eu estudo
card (card-body, card-title, card-actions)	Seção "Projetos": três cards, um para cada atividade que eu já fiz
alert (alert-info)	Seção "Contato", com uma informação de contato
input, textarea e fieldset	Formulário de contato (nome, e-mail e mensagem)
toggle com theme-controller	Navbar, para alternar entre o tema claro e o escuro
footer (footer-center)	Rodapé da página
2. Por que escolhi navbar e hero no cabeçalho

Usei os dois porque eles resolvem coisas diferentes. A navbar fica fixa no topo e serve para navegar: mesmo no fim da página, dá para voltar para outra seção ou ir direto para o contato. Já o hero é a primeira coisa que a pessoa vê, e ali eu me apresento e coloco os dois botões principais.

Se eu usasse só a navbar, a página começaria direto no texto, sem um destaque. Se usasse só o hero, ficaria mais difícil de navegar. Juntos, a navbar organiza e o hero apresenta.

3. Pontos de ajuste com Tailwind
Cor dos botões: os botões do DaisyUI ficam com a cor do tema, e eu queria todos rosa. Mantive as classes btn-primary e btn-outline e acrescentei classes do Tailwind por cima, como bg-pink-600 border-pink-600 text-white. Assim o DaisyUI continua dando o formato do botão, e o Tailwind troca só a cor. Fiz isso nos botões e não no tema inteiro, porque assim o resto da página segue as cores do tema.
Grade dos cards: o DaisyUI cria o card, mas não organiza vários cards lado a lado. Usei grid grid-cols-1 md:grid-cols-3 gap-6 do Tailwind: uma coluna no celular e três colunas no computador.
Navbar no celular: usei hidden md:flex para esconder os links do centro em telas pequenas, senão eles não cabem, e sticky top-0 para a navbar acompanhar a rolagem.
Largura e centralização: as seções usam max-w-3xl, max-w-5xl e mx-auto para o texto não ficar esticado em telas grandes.
4. Reflexão sobre temas

Testei dois temas: o light (claro) e o dark (escuro), trocando o data-theme. Os dois funcionam, porque as cores do fundo, do texto e dos cards vêm das classes do DaisyUI (bg-base-100, bg-base-200, text-base-content) e acompanham o tema sozinhas.

Na minha opinião, o tema claro ficou mais coerente com o conteúdo. A página é uma apresentação leve, com botões rosa, e o fundo claro deixa o rosa mais evidente. No escuro, o texto continua legível, mas o rosa dos botões perde um pouco do destaque.

# ATIVIDADES ANTERIORES
## Tarefa 10 – Seção de eventos

**Objetivo:** A partir do código HTML limpo (sem classes), você deve adicionar classes Tailwind para estilizar a seção "Eventos" do site do IFRN, reproduzindo o layout da imagem de referência.


### regras

- Use apenas classes utilitárias do Tailwind – sem CSS customizado.
- Não modifique a estrutura HTML (tags, conteúdo, atributos href, src, etc.).
- Consulte o Cheatsheet para encontrar as classes adequadas.


---

## Passo a passo para execução

1. **Atualize seu fork** do repositório da turma.
2. **Crie uma nova branch** para esta tarefa:  
   ```bash
   git checkout -b features/atividade-10-evento
   ```
3. **Insira classes Tailwind** em cada elemento para reconstruir o layout, visualizando como está o site do IFRN e criar a estrutura adequada com as classes mais proeminentes.
   
4. **Commit e push**:
   ```bash
   git add .
   git commit -m "Atividade 10 - Seção de eventos"
   git push origin atividade-9-footer
   ```

5.  **Envie o link da branch** no Google Sala de Aula.

## Dicas

- Use o **Cheatsheet** que foi fornecido para consultar rapidamente as classes.
- Utilize o **Tailwind Play** (https://play.tailwindcss.com/) para testar pequenos trechos.
- **Cores institucionais:**
  - Verde escuro: `#23472B`
  - Verde funcional: `#58B06B`
  - Verde claro (bordas): `#AAD8B5`
  - Fundo da seção: `#E8F2EC`
- **Status diferenciados:** "Em breve" e "Em andamento" devem ter cores diferentes para transmitir a informação visualmente.
- **Acessibilidade:** mantenha os `aria-hidden="true"` nos ícones e o `title` nos chips de campus.
- **Hover:** cada card deve ter um efeito sutil (sombra + borda mais forte) ao passar o mouse.


#### Container geral da seção
```html
<section class="bg-[#E8F2EC] py-16">
  <div class="max-w-7xl mx-auto px-4">
```

#### Cabeçalho (título + botão + descrição)
Aqui é uma parte do código, mas é preciso fazer os ajustes mais finos.

```html
<div class="flex flex-col md:flex-row md:items-center md:justify-between gap-4 mb-6">
  <h2 class="text-3xl md:text-4xl font-bold text-[#23472B]">Eventos</h2>
  <a href="/eventos/" class="inline-flex items-center gap-2 text-sm font-medium text-[#23472B] border border-[#23472B] rounded-full px-4 py-2 hover:bg-[#23472B] hover:text-white transition self-start md:self-auto">
    Todos os eventos
    <i class="ph ph-caret-right"></i>
  </a>
</div>
<p class="text-[#3A3A3A] max-w-3xl mb-10 leading-relaxed">...</p>
```

#### Grade de cards
```html
<div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6">
```
> 💡 Na imagem original aparecem 5 cards em uma linha, mas com `lg:grid-cols-4` você mantém um layout equilibrado. Para 5 colunas, use `lg:grid-cols-5`.

#### Cada card (link `<a>`)
```html
<a href="#" class="bg-white rounded-2xl border border-[#AAD8B5] p-5 flex flex-col gap-3 hover:shadow-md hover:border-[#58B06B] transition-all duration-200">
```

#### Status (span)
```html
<span class="inline-flex items-center gap-1 text-xs font-semibold text-[#23472B]">
  <i class="ph ph-warning"></i>
  Em breve
</span>
```
> Para "Em andamento", mude a cor e o ícone:
> ```html
> <span class="inline-flex items-center gap-1 text-xs font-semibold text-[#58B06B]">
>   <i class="ph ph-circle"></i>
>   Em andamento
> </span>
> ```

#### Chip de Campus
```html
<span class="inline-flex items-center gap-1 text-xs text-gray-600 border border-gray-200 rounded-full px-3 py-1 self-start">
  <i class="ph ph-buildings"></i>
  Pau dos Ferros
</span>
```

#### Título do evento
```html
<h3 class="text-base font-medium text-[#1A1A1A] leading-snug flex-1">
  Vivências em Arte
</h3>
```

#### Data (bloco com dia/mês/ano)
```html
<div class="flex items-end gap-2 mt-2">
  <span class="text-4xl font-bold text-[#23472B] leading-none">07</span>
  <div class="flex flex-col text-xs font-semibold text-[#23472B] uppercase">
    <span>dez</span>
    <span class="text-gray-500 font-normal">2026</span>
  </div>
</div>
```



o inverno está chegando

o inverno está chegando

