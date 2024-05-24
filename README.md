# operacoes-matematicas

read -p "Digite o primeiro número: " num1
read -p "Digite o segundo número: " num2


echo "Adição: $(echo "$num1 + $num2" | bc)"
echo "Subtração: $(echo "$num1 - $num2" | bc)"
echo "Multiplicação: $(echo "$num1 * $num2" | bc)"

if [ "$num2" == "0" ]; then
    echo "Divisão: Erro: Divisão por zero"
else
    echo "Divisão: $(echo "scale=2; $num1 / $num2" | bc)"
fi

chmod +x operacoes-matematica.sh
./operacoes-matematicas.sh
