img/x-special/nautilus-clipboard
copy
file:///home/wallaceferreirasilva/Imagens/imc-preview.jpg



# CalculadoraIMC
Aplicação simples desenvolvida em Java para cálculo do Índice de Massa Corporal (IMC), com classificação automática baseada nos padrões da OMS.

## 🚀 Funcionalidades
- Entrada de peso e altura via interface gráfica
- Cálculo automático do IMC
- Classificação do resultado:
  - Abaixo do peso
  - Peso ideal
  - Sobrepeso
  - Obesidade (graus I, II e III)

## 🛠 Tecnologias utilizadas
- Java
- JOptionPane (Swing)

## 📂 Estrutura do projeto


void main() {
    {
Locale.setDefault(Locale.US);
Scanner sc = new Scanner(System.in);
     double peso = Double.parseDouble(JOptionPane.showInputDialog("DIGITE SEU PESO"));
     double altura = Double.parseDouble(JOptionPane.showInputDialog("DIGITE SUA ALTURA"));
     double imc = peso / (altura * altura);

        String formatado = String.format("%.2f" , imc);
        if (imc < 18.5){
            JOptionPane.showMessageDialog(null, "O IMC do usuário é " + formatado + " ABAIXO DO PESO");

        } else if (imc >= 18.6 && imc <= 24.9) {
            JOptionPane.showMessageDialog(null, "O IMC do usuário é " + formatado + " PESO IDEAL (PARABÉNS)" );
        } else if (imc >= 25.0 && imc <= 29.9) {
            JOptionPane.showMessageDialog(null, "O IMC do usuário é " + formatado + " ATENÇÃO VOCÊ ESTÁ A CIMA DO PESO" );
        } else if (imc >= 30 && imc <= 34.9) {
            JOptionPane.showMessageDialog(null, "O IMC do usuário é " + formatado + " OBESIDADE GRAU I" );

        } else if (imc >= 35.0 && imc <= 39.9) {
            JOptionPane.showMessageDialog(null, "O IMC do usuário é " + formatado + " OBESIDADE GRAU II" );

        }else {
            JOptionPane.showMessageDialog(null, "O IMC do usuário é " + formatado + " OBESIDADE GRAU III" );

        }
        sc.close()
    }
}

