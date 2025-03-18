<h2><a href= "https://www.mackenzie.br">Universidade Presbiteriana Mackenzie</a></h2>
<h3><a href= "https://www.mackenzie.br/graduacao/sao-paulo-higienopolis/ciencia-da-computacao">Ciência da Computação</a></h3>


<font size="+12"><center>
*&lt;FALCÃO SOMBRIO&gt;*
</center></font>

**Conteúdo**

- [Autores](#nome-alunos)
- [Descrição do Projeto](#introdução-do-projeto)
- [Análise de Requisitos Funcionais e Não-Funcionais](#descrição-dos-requisitos)
- [Diagrama de Atividades](#diagrama-de-atividades) 
- [Diagrama de Casos de Uso](#diagrama-de-comportamento-atores)
- [Descrição dos Casos de Uso](#descrição-das-funcões)
- [Diagrama de Senquencia](#diagrama-de-ordem-interações)
- [Diagrama de Classes](#diagrama-orientado-objetos)
- [Diagrama de Estados](#diagrama-estrutura-componente)
- [Diagrama de Implantação](#diagrama-de-hardware-software)
- [Referências](#referências)


# Autores

* Bruna Soncini Nunes
* Gabriel Nottoli Buck
* Joao Vitor Rocha Miranda
* Julia Andrade


# Descrição do Projeto

A Securus Dynamics é uma empresa multinacional que desenvolve drones bélicos autônomos para operações militares. Seu principal produto, o Aquila-X, usa IA e sensores avançados para missões táticas, reconhecimento e ataques de precisão.

A empresa está criando o **Falcão Sombrio**, um novo sistema para controle remoto e autônomo dos drones via rede distribuída e interface avançada. O projeto enfrenta desafios em sistemas operacionais (tempo real, segurança e concorrência) e banco de dados (armazenamento distribuído, replicação e auditoria).

Devido a falhas na arquitetura atual, a empresa contratou a **Cyber Bullet System (Turma 4G)** para redesenhar o software e o banco de dados que suportam as operações críticas dos drones.

# Análise de Requisitos Funcionais e Não-Funcionais
## Introdução 

O **Sistema Falcão Sombrio** tem como objetivo permitir a operação remota e autônoma de drones militares através de uma infraestrutura distribuída e uma interface operacional avançada. O sistema deve garantir segurança, eficiência e confiabilidade em missões táticas, reconhecimento em território hostil e ataques de precisão. O sistema será baseado em uma arquitetura distribuída, garantindo maior confiabilidade e disponibilidade.

O sistema abrange as seguintes funcionalidades principais:
- Controle de drones via interface remota e operações autônomas.
- Sensoriamento inteligente para navegação, detecção e evasão de ameaças.
- Gerenciamento de comunicação em tempo real e protocolos de fallback para evitar falhas.
- Banco de dados seguro e distribuído, com logs de auditoria imutáveis.
- Autenticação avançada para garantir acesso autorizado.

O sistema tem como público alvo:
- Operadores militares responsáveis pelo controle dos drones.
- Engenheiros de software e segurança encarregados da manutenção e evolução do sistema.
- Arquitetos de software focados na infraestrutura distribuída e no gerenciamento de dados.

## Descrição Geral
O projeto envolve desafios de sistemas operacionais (tempo real, segurança e concorrência), além de banco de dados (armazenamento distribuído, replicação e logs de auditoria). A Consultoria Cyber Bullet System deve reformular toda a arquitetura de software e definir um novo modelo de
banco de dados para suportar as operações críticas dos drones. 

## Requisitos Funcionais e Não Funcionais
### Requisitos Funcionais (O que o sistema deve fazer)

1 → Central de Controle

A interface de gerenciamento de frotas de drones é um requisito funcional porque define uma funcionalidade essencial do sistema: permitir que operadores interajam com os drones. O mesmo vale para o controle remoto e autônomo dos drones e o dashboard de telemetria, pois são ações diretas realizadas pelo sistema para cumprir seu propósito.

2 → Sistema de Navegação Inteligente

O sensoriamento do ambiente por LIDAR, câmeras e GPS, junto com a detecção e evasão de ameaças, são funções essenciais para garantir que os drones operem de forma autônoma e segura. Como esses recursos definem o comportamento esperado dos drones, eles são requisitos funcionais.

3 → Gerenciamento de Comunicação

A comunicação segura e em tempo real entre os drones e a central de controle é uma funcionalidade essencial para garantir o comando e controle remoto. Além disso, a existência de um mecanismo de fallback para evitar perda de conexão assegura que o sistema possa continuar operando mesmo em condições adversas.

4 → Banco de Dados e Auditoria

O armazenamento de logs de missões e eventos críticos permite o rastreamento das operações dos drones, garantindo histórico para auditorias. Como essa funcionalidade é parte do escopo do sistema, ela é um requisito funcional.

5 → Sistemas Embarcados e Segurança

A autenticação de operadores via biometria e autenticação multifator é uma função específica do sistema para garantir acesso seguro. Da mesma forma, o monitoramento do SO embarcado evita falhas operacionais nos drones, tornando-se um requisito funcional do sistema.

### Requisitos Não Funcionais (Como o sistema deve operar)

1 → Desempenho e Confiabilidade

A exigência de minimizar latência e evitar interrupções não define uma função específica do sistema, mas sim um critério de qualidade. Da mesma forma, a implementação de failover automático não é uma funcionalidade isolada, mas sim uma garantia de confiabilidade.

2 → Segurança

A criptografia de ponta e as assinaturas digitais não são ações diretas que o sistema executa para cumprir sua finalidade, mas sim garantias de proteção de dados e resistência a ataques. Os logs de auditoria imutáveis também garantem a segurança, mas não representam uma funcionalidade visível do sistema.

3 → Gerenciamento de Banco de Dados

Garantir a integridade e sincronização dos dados em tempo real não é uma funcionalidade específica, mas sim um critério de qualidade do sistema. O uso de banco de dados distribuído e replicado também não é uma função visível para o usuário, mas sim um requisito que garante a robustez do sistema.

4 → Sistemas Operacionais e Concorrência

O gerenciamento eficiente de múltiplas threads e a priorização de processos são preocupações de desempenho e otimização do sistema. Embora sejam essenciais para o funcionamento do sistema, elas não representam uma funcionalidade específica que o usuário final pode acessar diretamente, tornando-se um requisito não funcional.


## Interfaces do Sistema
### Telas e Interações Principais
- Tela de Login para autenticação via usuário e senha, com suporte a biometria.
- Painel de Controle para visualização e controle da frota de drones.
- Tela de Missão para exibir a rota, status da missão e eventos críticos em tempo real.
- Tela de Logs para histórico de operações, falhas e outros eventos críticos.

## Restrições
Tecnológicas:
- O sistema deve operar em uma arquitetura distribuída com bancos NoSQL.
- O sistema deve suportar protocolos seguros de comunicação em tempo real.

Legais:
- O sistema deve seguir normas de cibersegurança e proteção de dados militares.

Operacionais:
- O sistema deve ser capaz de operar em ambientes hostis, sem conexão constante com servidores centrais.

## Critérios de Aceitação
- Garantir a continuidade da operação entre servidores e componentes do sistema (failover).
- Garantir a operação dos drones em situações de falha de comunicação (fallback).
- Todos os eventos críticos devem ser registrados corretamente nos logs de auditoria.
- O sistema deve impedir acesso não autorizado e tentativas de invasão devem ser detectadas.
- A interface deve exibir dados de telemetria em tempo real.


# Diagrama de Atividades

*&lt;Diagrama para visualizer as pessoas das áreas de negócios e de desenvolvimento de uma organização para entender o processo e comportamento.&gt;*

# Diagrama de Casos de Uso

*&lt;Diagrama para visualizar o comportamento dos atores&gt;*

# Descrição dos Casos de Uso

*&lt;Descrição do comportamento entre os atores/resquisitos&gt;*

# Diagrama de Sequência

*&lt;Diagrama de ordem e interação dos objetos&gt;*

# Diagrama de Classes

*&lt;Diagrama de relacionamento entre classes para os seus atributos e operações&gt;*

# Diagrama de Estados

*&lt;Diagrama para permite modelar o comportamento interno de um determinado objeto, subsistema ou sistema global&gt;*

# Diagrama de Implantação

*&lt;Diagrama para exibir o relacionamento de hardware e software no projeto&gt;*

# Referências

*&lt;Lista de referências&gt;*
