# E - CPU

| Entrega      |
|--------------|
| Terça - 25/04 |

![](../figs/G-CPU/sistema-cpu.svg)

Nesse projeto cada grupo terá que implementar sua própria CPU do Z01. 

## Começando

A seguir explicações de como começar o projeto.

### Entendendo a Organização do Projeto

A pasta do projeto E no repositório Z01, possui a seguinte estrutura:

```
E-Computador/
    testeHW.py
    src/
    Quartus/
```

1. `testeHW.py`: Testa o `controlUnit.vhd`, `memoryIO.vhd` e `CPU.vhd` (todo o HW do computador)


### Testando HW 

Abra o terminal na pasta `E-Computador`, deixe descomentado apenas as linhas referentes ao respectivo módulo (`ControlUnit.vhd`, `MemoryIO.vhd` e/ou `CPU.vhd`) no arquivo `config_testes.txt` e execute o script python:

```bash
$ ./testeHW.py
```

> O teste do CPU apenas funcionará se o ControlUnit tiver sido implementado.

Todos os módulos vhdl (desde o projeto B) serão compilados e o `CPU.vhd` será executado. 


### Actions

Adicione ao Actions o teste:

- `testeHW.py`

!!! tip
    No Actions você tem que colocar o caminho completo: `E-Computador/...`


## Projeto

Deve-se implementar o `Control Unit` e integrar os módulos: `MemoryIO` e `CPU`. 


## Módulos 

!!! note
    Esses arquivos estão localizados em `E-Computador/src/`

Os módulos estão listados de maneira Top - Down

<!--
---------------------------
 
- Computador (==já está pronto! Não precisa mexer==, mas é legal ver!)
    - **Arquivo**: `computador.vhd`
    - **Descrição**: TopLevel do projeto, entidade que integra a memória ROM o MemoryIO, CPU e PLL
    - **Dependências**:
         - `Dispositivos/ROM/ROM32K.vhd`: ROM a ser utilizada no projeto (já foi dado pronto)
         - `Dispositivos/PLL/PLL.vhd`: PLL a ser utilizada no projeto (já foi dado pronto)
    
---------------------------
-->

- MemoryIO
    - **Arquivo**   : `MemoryIO.vhd`
    - **Descrição** : Faz o mapa de memória para a CPU.
    - **Dependências** :
         - `.Dispositivos/RAM16K.vhd` : RAM a ser utilizada no projeto (já foi dado pronto)
         - `.Dispositivos/Screen.vhd` : Controlador do LCD a ser utilizada no projeto (já foi dado pronto)
    
---------------------------

- CPU
    - **Arquivo**   : `CPU.vhd`
    - **Descrição** : CPU do Z01 integra registradores, controlUnit, ULA e PC.
    - **Dependências** :
         - `ControlUnit.vhd` : Unidade de controle a ser implementada
         - `ULA.vhd` : Unidade lógica desenvolvida no projeto D
         - `PC.vhd` : Program counter do projeto E
         - `register16.vhd`, `mux16.vhd` : Componentes do projeto C e D 

---------------------------

- ControlUnit
    - **Arquivo**   : `ControlUnit.vhd`
    - **Descrição** : Unidade de controle da CPU do Z01.
    - **Dependências** :
         - não há 
         
### Diagramas 

---------------------------

![MemoryIo.vhd](../figs/G-CPU/memoryIO.png)

---------------------------

![ControlUnit.vhd](../figs/G-CPU/controlUnit.svg){width=400}

---------------------------

## Rubrica do projeto

!!! warning
    Os conceitos B e A devem ser feitos em um outro branch!
    
    - `git checkout -B CPU-Extras`

| Conceito |                                                                                     |
|----------|-------------------------------------------------------------------------------------|
| I        |  Menos da metade dos módulos funcionando                                           |
|          |                                                                                    |
| D        |  Ao menos um módulo não está feito e não passa no testes.                          |
|          |                                                                                    |
| C+       |  Construiu com os módulos do grupo o seu próprio computador                        |
|          |  Todos os módulos sendo testados no Actions.                                       |
|          |  Todos os módulos passando nos testes.                                             |
|          |                                                                                    |
| B+       |  Adiciona um novo registrador a CPU  (`%S`)                                        |
|          |  Modifica os testes para testar esse novo recurso!                                 |
|          |                                                                                    |
| A+       |  Possibilita realizar carregamento efetivo em %D (`leaw $5, %D`)                   |
|          |  Modifica os testes para testar esse novo recurso!                                 |


> O grupo deve avaliar o melhor local para colocar o registrador %S e como fazer o carregamente em %D (Há mais de uma forma).

### Testagem mais completa na próxima APS

Para testar o computador de uma forma mais completa, iremos executar os programas realizados na APS `F-Assembly` no Harware que vocês montaram. 

### Formulários

- [Scrum Master](https://forms.gle/KGFbHLrSzf26HCs19)
- [Desenvolvedores](https://forms.gle/1Cq2kS5hWZpnQBqU7)
 

