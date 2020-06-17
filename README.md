![last commit badge](https://badgen.net/github/last-commit/fddaineze/NativeScript-App-Example) ![license badge](https://badgen.net/github/license/fddaineze/NativeScript-App-Example) ![commits badge](https://badgen.net/github/commits/fddaineze/NativeScript-App-Example) ![github badge](https://badgen.net/badge/icon/github?icon=github&label)

## UTILIZANDO NATIVESCRIPT + VUE PELA PRIMEIRA VEZ (Windows)

- [Documentação Oficial](https://docs.nativescript.org/start/quick-setup)
1. [Instalação-do-pacote](#1.-Instalação-do-pacote)
2. [Instalação do NativeScript CLI](#2.-Instalação-do-NativeScript-CLI)
3. [Criando o Projeto](3.-Criando-o-Projeto)
4. [Iniciando via VSCODE](4.-Iniciando-via-VSCODE)
5. **[Resumo de comandos*](5.-Resumo-de-comandos)**

#### 1. Instalação do pacote
Primeiramente é necessário executar a linha de comando abaixo em modo **administrador**

> ###### *Pressione a tecla Windows > Digite "CMD" > Botão direito > Executar como administrador*

```bash
@powershell -NoProfile -ExecutionPolicy Bypass -Command "iex ((new-object net.webclient).DownloadString('https://www.nativescript.org/setup/win'))"
```

Durante a instalação, pode ser necessário aceitar um prompt de Controle de Conta de Usuário para conceder privilégios administrativos ao script.

Este comando verifica se os softwares necessários estão instalados, caso sim, apenas pula a etapa e em caso negativo realiza a instalação. Após a instalação, você terá:

- A última release oficial estável do Node.js (LTS) 8.x
- Google Chrome
- JDK 8
- Android SDK
- Android Support Repository
- Google Repository
- Android SDK Build-tools 28.0.3 ou uma versão superior estável e oficial
- Android Studio

#### Obs: confira se as variáveis de ambiente do JAVA estão corretamente configuradas:

As duas variáveis ​​de ambiente `JAVA_HOME` e `ANDROID_HOME` são necessárias para o desenvolvimento em Android, que deveriam ter sido automaticamente adicionadas como parte da instalação:

- Feche qualquer janela de comando do windows
- Abra uma nova janela de comando
- execute `echo %JAVA_HOME%` and make sure a valid path is returned
- execute `echo %ANDROID_HOME%` and make sure a valid path is returned

#### 2. Instalação do NativeScript CLI

A instalação do NativeScript CLI é realizada via npm, portanto, não há segredo:
```bash
npm install -g nativescript
```
Será necessário também o vue/cli, caso não o tenha instalado, execute:
```bash
npm install -g @vue/cli
```

#### 3. Criando o Projeto

Vamos começar com o template basico para **VUE** (lembrando que nativescript trabalha com outros frameworks também)
```bash
vue init nativescript-vue/vue-cli-template helloworld
```
Acesse o diretorio
```bash
cd helloworld
```
E instale todas as dependências necessárias (repare que a criação do projeto foi rápida)
```bash
npm install
```

#### 4. Iniciando via VSCODE

Após a conclusão, abra o vscode pelo comando `code .` e execute em seu terminal:
```bash
tns run android --bundle
```

O tns irá construir o projeto, compilando e instalando a aplicação no emulador e, após isso, iniciando a aplicação automaticamente. O tns fica então executando no terminal, observando qualquer alteração nos arquivos do projeto.

> Dica: Ative a depuração USB em seu celular e conecte via usb, isso será o suficiente para que o programa execute diretamente nele

#### 5. Resumo de comandos

```bash
@powershell -NoProfile -ExecutionPolicy Bypass -Command "iex ((new-object net.webclient).DownloadString('https://www.nativescript.org/setup/win'))"

npm install -g nativescript

npm install -g @vue/cli

vue init nativescript-vue/vue-cli-template helloworld

cd helloworld

npm install

tns run android --bundle
```

#### Extra

Para emular o android diretamente no computador, recomendo o uso do Genymotion, que possui um plano free para uso pessoal
