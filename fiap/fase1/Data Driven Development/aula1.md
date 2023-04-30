# DDD
## AULA 1

### Introdução
> Adequar arquitetura ao negócio.

### Domínios
- É o principal motivo daquele negócio.
  - Ex: O domínio de uma escola é a educação.

#### Subdomínios Principais
- O que faz o negócio especial, o que faz de diferente dos outros.
  - Ex: Escola são **Aulas e Metodologias**
    - Netflix são os **Vídeos**

#### Subdomínios Genéricos
> Depende do contexto, o que é um **Subdomínio Generico** para um **Dóminio** pode **NÃO** ser para outro.
- Conjunto de processos que são comuns no mercado.
- São complexos e difíceis de implementar, possuem **regras de negócio** e podem ser **únicas** mas _NÃO apresentam vantagem para o negócio_. _NÃO diferencia o produto da empresa_
  - Ex: Escola é a *criptografia aplicada aos dados*
    - Netflix é a parte do *faturamento*

#### Subdomínios de Suporte
- Apoia o negócio da empresa, mas **NÃO** como **Subdomínio Principal**
- **NÃO** da vantagem estratégica  para o negócio, ele **COMPLEMENTA** o **Subdomínio Principal**
  - Ex: Escola é a gestão de pais e alunos.
    - Netflix é o cadastro de filmes e séries

#### Identificando Subdomínios
![como identificaar](https://vladikk.com/images/domains/flowchart.png)


#### Domain Expert
- Pessoa que tem conhecimento do **negócio**
- Detectou inicialmente a necessidade
- Capaz de descrever todos os processos e procedimentos que estão sendo implementados.
> Em um **Dóminio** com vários **Subdomínios** teremos diversos **Domain Experts**.
