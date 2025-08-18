1(Criar Projeto) - Entrar na pasta pelo terminal;{ 1.1 - Criar projeto > digitar
no terminal (npm create vite@latest); 1.1.1 - Dar nome ao projeto; 1.1.2 -
React; 1.1.3 - TS+SWC; }

2 - Abrir a pasta do projeto no VsCode;

3(Criar arquivo de configuração) - Dentro da pasta do projeto, criar um 'new
folder'(.vscode); 3.1 - dentro dessa nova pasta criar um 'new
file'(settings.json) Exemplo de Configurações:

        {
        "window.zoomLevel": -1, // tamanho da tela
        "breadcrumbs.enabled": true, // apa
        "editor.fontSize": 18, // tamanho da área de trabalho
        "debug.console.fontSize": 18,
        "terminal.integrated.fontSize": 18,
        "editor.glyphMargin": false,
        "workbench.activityBar.location": "hidden",
        "editor.lineNumbers": "on", // mostra os numeros das linhas

        "files.eol": "\n", // Final de linha sempre será LF

        // 🛠 Formatação e Lint
        "editor.defaultFormatter": "esbenp.prettier-vscode",
        "editor.formatOnSave": true,

        "editor.codeActionsOnSave": {
            "source.fixAll.eslint": "explicit"
        },
        "[javascript]": {
            "editor.defaultFormatter": "esbenp.prettier-vscode"
        },
        "[typescript]": {
            "editor.defaultFormatter": "esbenp.prettier-vscode"
        },
        "[xml]": {
            "editor.defaultFormatter": "esbenp.prettier-vscode"
        },
        "[svg]": {
            "editor.defaultFormatter": "esbenp.prettier-vscode"
        },
        "[html]": {
            "editor.defaultFormatter": "esbenp.prettier-vscode"
        }
        }

4(Criar arquivo de configurações do Prettier) - Dentro da pasta do projeto
(prettierrc.json); Exemplo de configurações:

    {
        "arrowParens": "avoid", (Remove parênteses quando função arrow tem só 1 parâmetro.)
        "bracketSpacing": true, (Adiciona espaço dentro de chaves { assim })
        "htmlWhitespaceSensitivity": "css", (Segue as regras de espaço do CSS ao formatar HTML.)
        "insertPragma": false, (Não adiciona comentário especial (@format) no topo do arquivo.)
        "jsxBracketSameLine": false, (Em JSX, > de fechamento vai para nova linha.)
        "jsxSingleQuote": true, (Usa aspas simples em atributos JSX.)
        "printWidth": 80, (Quebra linhas acima de 80 caracteres.)
        "proseWrap": "always", (Sempre quebra linhas em textos (Markdown, etc.).)
        "quoteProps": "as-needed", (Só coloca aspas em propriedades de objeto quando necessário.)
        "requirePragma": false, (Não exige comentário especial para formatar o arquivo.)
        "semi": true, (Coloca ponto e vírgula no final das linhas.)
        "singleQuote": true, (Usa aspas simples em vez de duplas.)
        "tabWidth": 2, (Usa aspas simples em vez de duplas.)
        "trailingComma": "all", (Coloca vírgula no final de listas/objetos/múltiplas linhas)
        "useTabs": false (Usa espaços em vez de tabulação real.)
    }

5(Continuar a instalação) - No terminal do vsCode; 5.1 - npm install (irá
instalar os pacotes do package.json)

6(rodar o projeto) - npm run dev;

7(Configuração GitHub) - 7.1(Configurar SSH-keygen.exe(chave publica/privada)) -
Essa parte eu escrevo depois; 7.2 - Criar novo repositório no gitHub; 7.3 -
Copiar chave ssh do repositório; 7.4 - (Configurações git no vsCode):

    {
        "git init" - iniciar o git na pasta do projeto;
        "git branch -m main" - trocar o nome da branch para main;
        "git config user.name "Hugo Rodrigues"" - configurar user;
        "git config user.email "hugorbrdev@gmail.com" - configurar email;
        "git config core.eol lf" - configurar LF;
        "git config core.autocrlf input";
        "git config --list --local" - mostra todas as configurações feitas localmente;
        "git add ." - Adicionar todos os arquivos no git;
        "git commit -m "menssagem" - COMMIT;
        "git push" - mandar pro gitHub PUSH
        "git push origin main -u" - PUSH (depois desse comando usando o -u, só basta fazer git push)
        "git status" - status;
        "git reset --hard" - RESET Voltar o projeto para o commit salvo
        "git remote add origin 'link ssh'" - adicionar conexão com repositório do gitHub

    }

8 (Criando componentes) - Dentro da pasta 'src' criar um arquivo 'App.tsx';
8.1 - Exemplo de formato:

    {
        export function Nome do Componente() {
        console.log('Oi');
        return (
        <> // essas <> estão aí, pois um componete pode retornar apenas um elemento
            <h1>Hello World!</h1>
            <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Corporis,
            labore soluta sapiente at iste blanditiis nihil officiis facere fugiat
            deleniti recusandae ipsam assumenda molestiae sed, sequi cum fuga
            placeat iure.
            </p>
        </>
        );
        }
    }

9 (Criando o CSS) - Existem formas de criar o CSS:

    { 9.1(De forma global): Dessa forma o arquivo pode ser aplicado a qualquer elemento da página:

        {
            Dentro de src, crie uma pasta (styles), dentro dela crie os arquivos (global.css e theme.css) onde no (theme.css) ficam as variaveis - dessa forma, apenas alterando uma cor (ex: primary) altera em todo o projeto automaticamente. E então importe os dois arquivos (global.css e theme.css) dentro do componente (import './styles/theme.css';
            import './styles/global.css';)
        }

    }
