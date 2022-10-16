# Advantages
Criando e configurando um ambiente limpo com typescript, eslint, commit-msg e jest



## Possiveis problemas

- para caso o husky ignore a validação do pré commit do git-commit-msg-linter: 
execute: `npx husky add .husky/commit-msg ".git/hooks/commit-msg \$1"`

- Para caso ocorra erro no  run test:staged: error Command failed with exit code 1.

Caso esteja usando yarn: 
 - Altere dentro do arquivo ".husky/pre-commit" de `npx lint-staged` para `yarn lint-staged`


Verifique se adicionou a frag `--passWithNoTests` junto ao script do jest: 

 ```
   "scripts": {
    "test": "jest --passWithNoTests",
    "test:staged": "jest --passWithNoTests"
  }
 ```

