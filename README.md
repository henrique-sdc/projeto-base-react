# Projeto Base React com Tailwind CSS, Lucide, ShadCN e TypeScript

Este repositório serve como um ponto de partida pré-configurado para projetos React, economizando tempo e esforço na configuração inicial. Ele inclui as seguintes tecnologias e configurações:

## 🚀 Tecnologias

*   **Front-end:**
    *   [React](https://react.dev/) (v19): Biblioteca JavaScript para construir interfaces de usuário.
    *   [TypeScript](https://www.typescriptlang.org/) (v5.5.2 ou v4.9.5): Superset do JavaScript que adiciona tipagem estática.
    *   [Tailwind CSS](https://v3.tailwindcss.com/) (v3.4.17): Framework CSS utilitário para estilização rápida.
    *   [Lucide](https://lucide.dev/): Biblioteca de ícones SVG.
    *   [ShadCN](https://ui.shadcn.com/): Coleção de componentes reutilizáveis construídos com Tailwind CSS.
*   **Ferramentas:**
    *   [Node.js](https://nodejs.org/) (v22.14.0): Ambiente de execução JavaScript.
    *   [NPM](https://www.npmjs.com/) (v11.2.0): Gerenciador de pacotes do Node.js.
    *   [PostCSS](https://postcss.org/): Ferramenta para transformar CSS com JavaScript.
    *   [ESLint](https://eslint.org/): Ferramenta de linting para JavaScript/TypeScript.
    *   [Prettier](https://prettier.io/): Formatador de código.

## 💻 Extensões VS Code Recomendadas

*   Tailwind CSS IntelliSense
*   Prettier - Code formatter
*   ESLint
*   PostCSS Language Support

**Configurações VS Code:**

*   Defina "Prettier" como o formatador padrão ("Default Formatter").
*   Habilite a formatação automática ao salvar ("Format On Save").

## 📝 Configuração do ESLint

Este projeto já vem com o ESLint configurado.  Consulte a documentação para personalizações adicionais: [eslint-config-react-app](https://www.npmjs.com/package/eslint-config-react-app)

## 🛠️ Passos de Criação e Configuração (Para Referência)

Os passos abaixo descrevem como este projeto base foi criado.  Você **NÃO** precisa executá-los ao clonar este repositório, pois ele já está configurado.  Eles estão aqui para fins de documentação e referência.

1.  **Criação do Projeto:**
    ```bash
    npx create-react-app my-app --template typescript
    cd my-app
    npm start
    ```
    Documentação: [Create React App - Adding TypeScript](https://create-react-app.dev/docs/adding-typescript/)

2.  **Integração do Tailwind CSS (v3.4.17) com PostCSS:**
    ```bash
    npm install -D tailwindcss@3 postcss autoprefixer
    npx tailwindcss init
    ```
    Documentação: [Tailwind CSS v3 - Installation using PostCSS](https://v3.tailwindcss.com/docs/installation/using-postcss)

    *   **`tailwind.config.js`:**  Modifique o arquivo para incluir os caminhos dos seus arquivos de template.  (Já configurado neste projeto)
    *   **`postcss.config.js`:**  Crie este arquivo na raiz do projeto e adicione a configuração do PostCSS. (Já configurado neste projeto)
    *   **`src/App.css`:**  Remova o CSS padrão e adicione as diretivas do Tailwind.  (Já configurado neste projeto)
    *   **Importe `App.css`:**  Certifique-se de importar `'./App.css'` nos seus componentes.

3.  **Instalação do Lucide Icons:**
    ```bash
    npm install lucide-react
    ```
    Documentação: [Lucide - Installation](https://lucide.dev/guide/installation)

4.  **Instalação e Configuração do ShadCN:**
    ```bash
    npm install class-variance-authority clsx tailwind-merge lucide-react tw-animate-css
    ```
    *   **`tsconfig.json`:**  Adicione a configuração de caminhos ("paths") para o ShadCN. (Já configurado neste projeto)
    *   **`src/styles/globals.css`:**  Crie este arquivo e adicione os estilos globais do ShadCN. (Já configurado neste projeto)
    *   **`src/lib/utils.ts`:**  Crie este arquivo e adicione as funções utilitárias do ShadCN. (Já configurado neste projeto)
    *   **`components.json`:** Crie este arquivo na raiz do projeto e cole a configuração. (Já configurado neste projeto).
    
    Documentação: [ShadCN - Manual Installation](https://ui.shadcn.com/docs/installation/manual)

5. **Adicionando Componente Button (Exemplo):**
    ```bash
    npx shadcn@latest add button --force
    ```
    

## ⚠️ Observações Importantes

*   **Resolução de Caminhos (`@`):**  A configuração inicial para usar `@` como alias para caminhos de diretórios pode não funcionar corretamente.  Em alguns casos, você precisará ajustar manualmente os imports:
    *   **Exemplo:**  Substitua `import { cn } from "@/lib/utils";` por `import { cn } from "src/lib/utils";`

*   **Tailwind CSS v4:**  Este projeto usa a versão 3.4.17 do Tailwind CSS.  Se você precisar usar a versão 4, considere usar Vite com React ou Next.js.

*   **Estrutura de Pastas:**
    *   `src/`:  Código-fonte principal (componentes, estilos, etc.).
    *   `public/`:  Arquivos estáticos.
    *   `package.json`:  Dependências e scripts.
    *   `src/lib`: Funções utilitárias.
    *   `src/styles`: Estilos globais.

## 🏁 Começando

1.  **Clone este repositório:**
    ```bash
    git clone https://github.com/henrique-sdc/projeto-base-react.git
    cd <NOME_DA_PASTA>
    ```

2.  **Instale as dependências:**
    ```bash
    npm install
    ```

3.  **Execute o projeto:**
    ```bash
    npm start
    ```

Agora você tem um projeto React pré-configurado e pronto para começar a desenvolver! Bom desenvolvimento!
