<h2><a href= "https://www.mackenzie.br">Universidade Presbiteriana Mackenzie</a></h2>
<h3><a href= "https://www.mackenzie.br/graduacao/sao-paulo-higienopolis/sistemas-de-informacao">Sistemas de Informação</a></h3>


<font size="+12"><center>
*&lt;Nome do Projeto&gt;* : Escola Infinito (TIA 2)
</center></font>

**Conteúdo**

- [Autores](#nome-alunos)
- [Descrição do Projeto](#introdução-do-projeto)
- [Análise de Requisitos Funcionais e Não-Fucionais](#descrição-dos-requisitos)
- [Diagrama de Atividades](#diagrama-de-atividades) 
- [Diagrama de Casos de Uso](#diagrama-de-comportamento-atores)
- [Descrição dos Casos de Uso](#descrição-das-funcões)
- [Diagrama de Senquencia](#diagrama-de-ordem-interações)
- [Diagrama de Classes](#diagrama-orientado-objetos)
- [Diagrama de Estados](#diagrama-estrutura-componente)
- [Diagrama de Implantação](#diagrama-de-hardware-software)
- [Referências](#referências)


# Autores

* Guilherme Martins Silva RA: 10417140
* Gabriel Lazareti Cardoso RA: 10417353

# Descrição do Projeto

Dado a demanda da Escola Infinito, temos a tarefa de desenvolver um Sistema de Presenças que será implementado para turmas (de 20 e 30 alunos) do 1° ao 5° ano do Ensino Fundamental II. Cada turma tem um professor especifico, ou seja, cada professor terá um enviroment para a turma que ele leciona em especifico, no qual consegue realizar o controle da presença (alguns professores como por exemplo: Professores de inglês e Educação Física necessitaram ter acesso ao enviroment de todas as turmas).Os responsaveis também terão um enviroment onde é possível visualizar a quantidade de presença e faltas. O Sistema será acessado para computar falta ou presença no inicio das aulas e logo após o retorno do intervalo. O estudando terá que ter uma presença mínima de >75% para passar na materia.

# Análise de Requisitos Funcionais e Não-Funcionais
- Requisitos Funcionais:
  - Plataforma fácil e intuitiva.
  - Ter Login e Senha.
  - Gerar Relatorios de Faltas agrupados por data, ano de ensino turma, professor disciplina ou aluno.
  - Enviar notificações por email para os responsaveis em caso de faltas execissivas (presença < 80%).
  - Acessibilidade: garantir um sistema acessivel a toos os usuarios, incluindo pessoas com deficiencias, com recursos de acessibilidade como tamanho de fonte ajustavél.
  - Acesso a partir de qualquer navegador web, inclusive em dispositivos móveis.
- Não Funcionais:
  - Ter segurança para impedir acessos a dados sensiveis, ou acesso indevido possibilitando a alteração de dados.
  - Impossibilitar a visualização de relatorios de terceiros.
  - Sistema deve estar disponível a todo tempo.

# Diagrama de Atividades

*&lt;Diagrama para visualizer as pessoas das áreas de negócios e de desenvolvimento de uma organização para entender o processo e comportamento.&gt;*!
![Fluxogramas](https://github.com/user-attachments/assets/cc5cdaeb-2176-41e1-b4d3-f947287cf9a9)




# Diagrama de Casos de Uso

*&lt;Diagrama para visualizar o comportamento dos atores&gt;*
![Diagrama de caso de uso](https://github.com/user-attachments/assets/fed2ce2e-3426-4cc8-b090-1b69c82cc05f)



# Descrição dos Casos de Uso

*&lt;Descrição do comportamento entre os atores/resquisitos&gt;*
### Registrar Falta:

**Ator: Professor**

**Descrição: O professor registra a falta de um determinado aluno em uma aula/dia em dois momentos diferentes.**

**Fluxo básico:**

- O professor acessa a funcionalidade "Registrar Falta".
- O sistema apresenta a lista de turmas e alunos.
- O professor seleciona a turma e o aluno que faltou.
- O professor registra a falta do aluno na data atual.
- O sistema salva a informação de falta registrada.

### Relatório de Faltas:

**Ator: Professor**

**Descrição: Gera um relatório com informações consolidadas sobre as faltas.**

**Fluxo básico:**
- O usuário acessa a funcionalidade "Gerar Relatório de Faltas".
- O sistema apresenta acessibilidade de busca (aluno, turma, data, disciplina, professor).
- O usuário seleciona os filtros desejados.
- O sistema gera o relatório de acordo com os filtros.
- O usuário visualiza o relatório de faltas gerado.
- O ususario visuzaliza a porcentagem de falta

### Notificação:

**Ator:Pais/Responsaveis**

**Descrição: Envia uma notificação por e-mail aos pais/responsáveis sobre a situação de faltas do aluno.**

 **Fluxo básico:**
- O sistema verifica diariamente o percentual de faltas de cada aluno.
- Para alunos com percentual abaixo do limite definido, o sistema automaticamente aciona o caso de uso "Enviar Notificação".
- O sistema busca os dados de e-mail dos pais/responsáveis.
- O sistema envia a notificação por e-mail

 ### Acessibilidae:

**Ator: Sistema**

**Descrição: Permite configurar as opções de acessibilidade e outras configurações do sistema.**

**Fluxo básico:**
- O administrador acessa a tela de configurações do sistema.
- O administrador altera as configurações de fonte, contraste, notificações, entre outras na WEB ou no mobile
- O sistema salva as configurações aplicadas.
- O sistema permite modificar o registro de faltas

### Qualquer Site/WEB:

**Ator: Professor, Adm Sistema, Pais/Responsaveis**

**Descrição: Permite configurar as opções de acessibilidade e outras configurações do sistema.**

**Fluxo básico:**
- O administrador acessa a tela de configurações do sistema.
- O administrador coloca todas as faltas no sistema.
- No sistema é possivel visualizar as notificacoes por aplicativo ou pelo site
- Professores e pais podem acessar o site pelo ID do aluno ou ID do professor
- Pais e professores veem a quantidade de falta
- Pais podem justificar a falta dos filhos com atestado

### Tabela da Descrição dos Casos de Uso
![image](https://github.com/user-attachments/assets/682faec6-b493-4bba-90f9-032b742916cf)

# Diagrama de Sequência
Sistema de chamada:
![Diagrama de sequência básico](https://github.com/user-attachments/assets/29f2e8ed-cfb6-43f5-bac2-81bf66da6887)

Gerador relatório:
![Diagrama de sequência básico (1)](https://github.com/user-attachments/assets/f54bdc16-7d58-4701-8f74-0f2be5ecb073)

E-mail automático(relatório):
![Diagrama de sequência básico](https://github.com/user-attachments/assets/86441a49-7ad2-4a4e-bf98-ff772244f8b3)

# Diagrama de Classes
![image](https://github.com/user-attachments/assets/cf22cd4e-9aeb-41cc-9bbb-21922da93fbd)


# Diagrama de Estados

*&lt;Diagrama para permite modelar o comportamento interno de um determinado objeto, subsistema ou sistema global&gt;*
