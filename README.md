# Super Trunfo - Cadastro de Cartas em C

## 📝 Descrição

Este programa em C permite cadastrar e exibir os dados de **duas cartas do Super Trunfo**, simulando um mini-cadastro de cidades para um jogo. O usuário insere informações como estado, código da carta, nome da cidade, população, área, PIB e número de pontos turísticos. Após o cadastro, o programa exibe as informações de cada carta de forma organizada.

---

## 🚀 Funcionalidades

- Cadastro de **duas cartas** com todos os dados necessários.
- **Exibição clara e formatada** das informações cadastradas.
- Interface simples, ideal para iniciantes em programação C.

---

## 🛠️ Como Usar

### Instalação do Compilador e Execução do Programa

---

### Para Linux

#### 1. Instalar o compilador GCC

Na maioria das distribuições Linux, o GCC já vem instalado. Caso não esteja, instale-o usando o gerenciador de pacotes:

- **Debian/Ubuntu:**
```
sudo apt update
sudo apt install build-essential
```
- **Fedora:**
```
sudo dnf groupinstall "Development Tools"
```
- **Arch Linux:**
```
sudo pacman -S base-devel
```

#### 2. Compilar o programa

No terminal, navegue até a pasta onde está o arquivo `super_trunfo.c` e execute:
```
gcc super_trunfo.c -o super_trunfo
```

#### 3. Executar o programa

Ainda no terminal, execute:
```
./super_trunfo
```

---

### Para Windows

#### 1. Instalar o compilador GCC com MinGW-w64 (64 bits)

- Acesse o site oficial do MinGW-w64: [https://sourceforge.net/projects/mingw-w64/](https://sourceforge.net/projects/mingw-w64/)
- Baixe o instalador adequado para o seu sistema (exemplo: `mingw-w64-install.exe`).
- Execute o instalador e siga as instruções.
- Finalize a instalação. O caminho padrão geralmente será algo como:  
  `C:\Program Files\mingw-w64\x86_64-<versão>\mingw64\bin`
- Adicione o caminho da pasta `bin` do MinGW-w64 à variável de ambiente `PATH` do Windows:
  - Pesquise por **Variáveis de Ambiente** no menu Iniciar.
  - Edite a variável `PATH` e adicione o caminho da pasta `bin` do MinGW-w64 (exemplo: `C:\Program Files\mingw-w64\x86_64-<versão>\mingw64\bin`).
- Abra o Prompt de Comando (cmd) e verifique a instalação com:
    ```
    gcc --version
    ```
- Se aparecer a versão do GCC, o compilador está instalado e configurado corretamente para 64 bits.

#### 2. Compilar o programa

No Prompt de Comando, navegue até a pasta onde está o arquivo `super_trunfo.c`:

```
cd caminho\para\a\pasta
gcc super_trunfo.c -o super_trunfo.exe
```

#### 3. Executar o programa

Ainda no Prompt de Comando, execute:
```
super_trunfo.exe
```

---

### Usando Visual Studio Code (VS Code)

- Instale o VS Code: [https://code.visualstudio.com/](https://code.visualstudio.com/)
- Instale a extensão **C/C++** da Microsoft.
- Certifique-se que o compilador GCC (MinGW no Windows ou GCC no Linux/macOS) está instalado e no PATH.
- Abra a pasta do projeto no VS Code.
- Use o terminal integrado para compilar e executar:
    ```
    gcc super_trunfo.c -o super_trunfo
    ./super_trunfo # Linux/macOS
    super_trunfo.exe # Windows
    ```

## 🗃️ Estrutura dos Dados

Cada carta contém os seguintes campos:

| Campo                  | Tipo    | Exemplo           |
|------------------------|---------|-------------------|
| Estado (A-H)           | `char`  | A                 |
| Código da Carta        | `string`| A01               |
| Nome da Cidade         | `string`| São Paulo         |
| População              | `int`   | 12325000          |
| Área (km²)             | `float` | 1521.11           |
| PIB (bilhões de reais) | `float` | 699.28            |
| Pontos Turísticos      | `int`   | 50                |

---

## ⚙️ Detalhes Técnicos

- **Entrada de dados:**  
  - Utiliza `scanf` para números e `fgets` para strings (nome da cidade).
  - Limpeza do buffer de entrada com `getchar()` para evitar problemas de leitura.
- **Saída formatada:**  
  - Exibe valores numéricos com precisão fixa (ex: `Área: 1521.110 km²`).
- **Sem estruturas de repetição ou decisão:**  
  - O programa segue uma sequência linear de comandos, conforme o desafio.

---

## Exemplo de Uso

### Entrada

Ao executar o programa, o usuário verá prompts para inserir os dados das duas cartas. Exemplo:
```
DADOS DA CARTA 1:
Digite o Estado (uma letra de 'A' a 'H'): A
Digite o código da carta (letra do estado + número de 01 a 04, e.g., A01): A01
Digite o nome da cidade (pode incluir espaços): São Paulo
Digite o número de habitantes da cidade (valor positivo): 12325000
Digite a área da cidade em km² (valor positivo): 1521.11
Digite o PIB da cidade em bilhões de reais (valor positivo): 699.28
Digite o número de pontos turísticos da cidade (valor positivo): 50

DADOS DA CARTA 2:
Digite o Estado (uma letra de 'A' a 'H'): B
Digite o código da carta (letra do estado + número de 01 a 04, e.g., B02): B02
Digite o nome da cidade (pode incluir espaços): Rio de Janeiro
Digite o número de habitantes da cidade (valor positivo): 6748000
Digite a área da cidade em km² (valor positivo): 1200.25
Digite o PIB da cidade em bilhões de reais (valor positivo): 300.50
Digite o número de pontos turísticos da cidade (valor positivo): 30
```

### Saída

Após a entrada, o programa exibe:
```
DADOS DA CARTA 1:
Estado: A
Código: A01
Nome da Cidade: São Paulo
População: 12325000
Área: 1521.110 km²
PIB: 699.3 bilhões de reais
Número de pontos turísticos: 50

DADOS DA CARTA 2:
Estado: B
Código: B02
Nome da Cidade: Rio de Janeiro
População: 6748000
Área: 1200.250 km²
PIB: 300.5 bilhões de reais
Número de pontos turísticos: 30
```

---

## 📌 Observações

- **Simplicidade intencional:** O programa não compara cartas nem faz validações avançadas.
- **Foco em usabilidade:** Mensagens claras e interface amigável para iniciantes.
- **Desafio proposto:** Desenvolvido como exercício para iniciantes, sem uso de laços ou condicionais.

---

✨ Projeto desenvolvido como parte de um desafio de programação em C!
