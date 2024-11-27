# SA - Portugol
 Trabalho feito sobre meu setor na SA proposta


Pseudocódigo para o gerenciamento da folha de pagamento:

algoritmo "folha_de_pagamento_vetores"
var
   nomes: vetor[1..5] de caractere

   salarios_base: vetor[1..5] de real

   bonus: vetor[1..5] de real

   desconto_inss: vetor[1..5] de real

   desconto_ir: vetor[1..5] de real

   vale_transporte: vetor[1..5] de real

   vale_refeicao: vetor[1..5] de real
   
   salario_final: vetor[1..5] de real
   
   i: inteiro
   
inicio
   // Entrada de dados para 5 funcionários
   
   para i de 1 ate 5 passo 1 faca
   
      escreva("Digite o nome do funcionário ", i, ": ")
      
      leia(nomes[i])
      
      escreva("Digite o salário base de ", nomes[i], ": ")
      
      leia(salarios_base[i])
      
      escreva("Digite o bônus de ", nomes[i], ": ")
      
      leia(bonus[i])
      
      escreva("Digite o desconto do INSS de ", nomes[i], ": ")
      
      leia(desconto_inss[i])
      
      escreva("Digite o desconto do IR de ", nomes[i], ": ")
      
      leia(desconto_ir[i])
      
      escreva("Digite o vale-transporte de ", nomes[i], ": ")
      
      leia(vale_transporte[i])
      
      escreva("Digite o vale-refeição de ", nomes[i], ": ")
      
      leia(vale_refeicao[i])

      // Cálculo do salário final
      
      salario_final[i] := salarios_base[i] + bonus[i] - desconto_inss[i] - desconto_ir[i] - vale_transporte[i] - vale_refeicao[i]
      
   fimpara

   // Exibição dos resultados
   
   para i de 1 ate 5 passo 1 faca
   
      escreva("Funcionário: ", nomes[i], " - Salário Final: ", salario_final[i], " ")
      
   fimpara
   
fimalgoritmo




Pseudocódigo para o recrutamento e seleção de novos funcionários:

algoritmo "triagem_de_curriculos_vetores"

var

   nomes_candidatos: vetor[1..6] de caractere

   experiencia: vetor[1..6] de inteiro
   
   escolaridade: vetor[1..6] de caractere
   
   area_especializada: vetor[1..6] de caractere
   
   localizacao: vetor[1..6] de caractere
   
   status_candidatos: vetor[1..6] de caractere
   
   i: inteiro
   
inicio

   // Entrada de dados para 6 candidatos
   
   para i de 1 ate 6 passo 1 faca
   
      escreva("Digite o nome do candidato ", i, ": ")
      
      leia(nomes_candidatos[i])
      
      escreva("Digite a experiência de ", nomes_candidatos[i], " (em anos): ")
      
      leia(experiencia[i])
      
      escreva("Digite a escolaridade de ", nomes_candidatos[i], " (superior, médio, técnico): ")
      
      leia(escolaridade[i])
      
      escreva("Digite a área de especialização de ", nomes_candidatos[i], ": ")
      
      leia(area_especializada[i])
      
      escreva("Digite a localização de ", nomes_candidatos[i], ": ")
      
      leia(localizacao[i])

      // Triagem com base nos critérios
      
      se (experiencia[i] >= 2) então
      
         se (escolaridade[i] = "superior") então
         
            se (area_especializada[i] = "TI") então
            
               status_candidatos[i] := "Aprovado para entrevista"
               
            senao
            
               status_candidatos[i] := "Rejeitado"
               
            fimse
            
         senao
         
            status_candidatos[i] := "Rejeitado"
            
         fimse
         
      senao
      
         status_candidatos[i] := "Rejeitado"
         
      fimse
      
   fimpara

   // Exibição dos resultados da triagem
   
   para i de 1 ate 6 passo 1 faca
   
      escreva("Candidato: ", nomes_candidatos[i], " - Status: ", status_candidatos[i])
      
      escreva(" ") // Nova linha para cada candidato
      
   fimpara
   
fimalgoritmo
