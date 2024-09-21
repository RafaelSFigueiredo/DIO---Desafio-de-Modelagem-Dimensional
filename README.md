# DIO - Desafio de Modelagem Dimensional

## Objetivo
O desafio consiste em criar um diagrama dimensional utilizando o modelo de esquema em estrela (star schema) com base no diagrama relacional fictício fornecido, focando nos dados acerca dos professores.

**OBS:** Apesar de não ser parte do desafio, foram criadas colunas para informações que normalmente estariam presentes em um modelo real, como os nomes dos professores, das disciplinas e dos cursos, que não estão incluídos no diagrama relacional fictício.

## Modelagem
A tabela fato (*fact table*), **f_Professor**, contém colunas relacionadas diretamente aos professores, como os IDs da disciplina, do departamento e do curso de cada um. Esses campos correspondem às chaves primárias de três tabelas dimensão (*dimension tables*), sendo elas **d_Disciplina**, **d_Departamento** e **d_Curso**, respectivamente.

Como parte das regras do desafio, embora o modelo relacional fictício não contenha informações sobre datas, foi criada uma quarta tabela dimensão, **d_Data**, cujas colunas armazenam o mês e o ano em que um professor ofertou uma disciplina. Sua chave estrangeira é **idProfessor**.

