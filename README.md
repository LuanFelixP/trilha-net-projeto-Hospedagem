📌 DIO - Trilha .NET - Explorando a linguagem C#

Este repositório contém a solução para o desafio de projeto do módulo Explorando a Linguagem C# da DIO (Digital Innovation One)
.

🚀 Desafio de Projeto

O objetivo foi desenvolver um sistema de hospedagem de hotel, capaz de gerenciar suítes, hóspedes e reservas, aplicando as regras de negócio propostas no desafio.

O programa foi implementado em C#, explorando conceitos de classes, objetos, encapsulamento e validações.

📖 Contexto

O sistema é composto pelas seguintes classes principais:

Pessoa → representa um hóspede.

Suíte → representa a suíte escolhida.

Reserva → faz o relacionamento entre hóspedes e suíte.

O programa deve ser capaz de:

Registrar hóspedes em uma reserva.

Verificar se a suíte escolhida comporta a quantidade de hóspedes.

Calcular corretamente o valor da diária.

Aplicar 10% de desconto caso a reserva seja igual ou superior a 10 dias.

📌 Regras e Validações

❌ Não é permitido reservar uma suíte com capacidade menor que a quantidade de hóspedes (gera Exception).

✅ O método ObterQuantidadeHospedes deve retornar a quantidade total de hóspedes.

✅ O método CalcularValorDiaria deve retornar o valor da reserva (Dias reservados x Valor da diária).

✅ Caso a reserva seja >= 10 dias, aplicar 10% de desconto no valor final.

🗂️ Estrutura do Projeto

Pessoa.cs → Classe para representar o hóspede.

Suite.cs → Classe para representar a suíte, com capacidade e valor da diária.

Reserva.cs → Classe responsável por vincular hóspedes e suíte, além de calcular os valores.

Program.cs → Arquivo principal para execução e testes.

🖥️ Exemplo de Uso
// Criação de hóspedes
List<Pessoa> hospedes = new List<Pessoa>();
hospedes.Add(new Pessoa(nome: "Luan Felix"));
hospedes.Add(new Pessoa(nome: "Maria Silva"));

// Criação da suíte
Suite suite = new Suite(tipoSuite: "Premium", capacidade: 2, valorDiaria: 100);

// Criação da reserva
Reserva reserva = new Reserva(diasReservados: 12);
reserva.CadastrarSuite(suite);
reserva.CadastrarHospedes(hospedes);

// Exibindo informações
Console.WriteLine($"Hóspedes: {reserva.ObterQuantidadeHospedes()}");
Console.WriteLine($"Valor diária: {reserva.CalcularValorDiaria()}");

📚 Aprendizados

Implementação de orientação a objetos em C#.

Uso de listas e coleções.

Aplicação de validações de negócio.

Cálculo de valores com regras condicionais.

✍️ Desenvolvido como parte da Trilha .NET - DIO.
