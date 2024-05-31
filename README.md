# Cálculo-com-Poténcia-em-Ruby

Vou mostrar aqui, como criar um módulo em Ruby para calcular a terceira potência de até três números inseridos pelo usuário. Aqui está um exemplo de como você pode estruturar o código:

```ruby
module CalculoPotencia
  def self.ler_numeros
    numeros = []
    puts 'Insira até 3 números (ou "sair" para terminar):'
    while numeros.size < 3
      input = gets.chomp
      break if input.downcase == 'sair'
      numero = input.to_i
      numeros << numero if numero != 0 || input == '0'
    end
    numeros
  end

  def self.calcular_potencias(numeros)
    numeros.map { |numero| numero ** 3 }
  end
end

# Uso do módulo
numeros = CalculoPotencia.ler_numeros
potencias = CalculoPotencia.calcular_potencias(numeros)
puts "Os números elevados à terceira potência são: #{potencias}"
```

**Descrição do Código:**
- O módulo `CalculoPotencia` contém dois métodos:
  - `ler_numeros`: Solicita ao usuário que insira números até que três sejam inseridos ou o usuário digite 'sair'. Os números são armazenados em um array.
  - `calcular_potencias`: Recebe o array de números e retorna um novo array com cada número elevado à terceira potência.

**Como Usar:**
1. Execute o script em um ambiente Ruby.
2. Insira os números conforme solicitado.
3. O programa irá exibir os números elevados à terceira potência.

**Nota:** Este código assume que o usuário insere números válidos e utiliza a entrada padrão do Ruby (`gets`) para ler os números. A função `chomp` é usada para remover a nova linha do final da entrada, e `to_i` para converter a entrada em um inteiro. O método `map` é utilizado para aplicar a operação de potência a cada elemento do array.

Espero que este exemplo ajude a quem precisar, a entender como trabalhar com módulos e cálculos em Ruby.
