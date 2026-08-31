<<<<<<< HEAD
o inverno está chegando
=======
# Repositório da turma de Design Web 2026


## 4ª Semana

### Passo 1 – Criar a branch da atividade
Crie uma branch da atividade. 
```
git checkout -b atividade-1
```
### Passo 2 – Editar o arquivo index.html
Substitua o conteúdo do <body> pelo código abaixo (ou personalize):

```
<div class="max-w-sm bg-white rounded-lg shadow-lg p-6 text-center">
  <img src="https://picsum.photos/seed/1/100" alt="Foto de perfil" class="w-24 h-24 rounded-full mx-auto mb-4">
  <h2 class="text-2xl font-bold text-gray-800">Seu Nome</h2>
  <p class="text-gray-600 mt-2">Desenvolvedor Web em aprendizado</p>
  <button class="mt-4 bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded">
    Seguir
  </button>
</div>
```

## Passo 3 – Commit e push
```
git add index.html
git commit -m "adiciona card de perfil estilizado com Tailwind"
git push origin atividade-1
```

### Passo 4 – Enviar o link no Google Sala de Aula
- No GitHub, vá até seu repositório fork.
- No seletor de branches, escolha atividade-1.
- Copie a URL (ex: https://github.com/SEU_USUARIO/turma-design-web/tree/atividade-1).
- Cole esse link no campo de entrega da tarefa.


## 3ª Semana 

Fizemos algumas atividades, focados no Github. Criamos e clonamos nosso repositório principal.

### Passo 1 – Fork do repositório

- Acesse: https://github.com/professor/turma-design-web
- Clique no botão Fork (canto superior direito). Isso criará uma cópia na sua conta. 

### Passo 2 – Clonar o fork
Abra o terminal (Git Bash, PowerShell ou terminal integrado do VS Code) e execute

```
git clone https://github.com/SEU_USUARIO/turma-design-web.git
cd turma-design-web
```



Arquivo de codigo compartilhado

## 2ª Semana 

### Cartão de Apresentação – Bruno Nakamura

Projeto didático para ensinar a integração entre **HTML semântico** e **SCSS** (pré-processador CSS).

## Estrutura

projeto/

├── index.html 

├── scss/

└── style.scss 

└── css/

└── style.css # Arquivo gerado pelo SCSS (não edite jamais ou vai perder tudo para sempre)


## Como usar

1. **Clone ou baixe** os arquivos.
2. **Compile o SCSS** para CSS:
   - Com o Sass instalado: `sass scss/style.scss css/style.css --watch`
   - Ou use a extensão "Live Sass Compiler" no VS Code.
3. **Abra** o `index.html` no navegador.

## Personalize

- **Cores**: altere as variáveis no início do `style.scss` (`$color-primary`, `$color-secondary`, etc.).
- **Imagem**: substitua a URL placeholder (`https://via.placeholder.com/...`) pelo seu próprio avatar.
- **Conteúdo**: edite o HTML para mudar texto, tecnologias e links.

## Boas práticas aplicadas

- Tags HTML semânticas (`header`, `main`, `section`, `footer`)
- Atributos de acessibilidade (`role`, `aria-label`, `focus-visible`)
- Responsividade com mixins (mobile-first)
- Código SCSS organizado com variáveis e aninhamento
>>>>>>> b5746461799a51b37006d5da60d5669aca8446d1
