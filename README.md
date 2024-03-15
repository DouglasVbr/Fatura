# Fatura


package mainfatura;


public class MainFatura {

   // Método main para teste
    public static void main(String[] args) {
       
        // Criando uma instância de Fatura
        Fatura fatura = new Fatura("001", "Teclado", 2, 50.0);
        
        // Imprimindo informações da fatura
        System.out.println("Número do item: " + fatura.getNumeroItem());
        System.out.println("Descrição do item: " + fatura.getDescricaoItem());
        System.out.println("Quantidade: " + fatura.getQuantidade());
        System.out.println("Preço unitário: " + fatura.getPrecoUnitario());
        System.out.println("Valor da fatura: " + fatura.getValorDaFatura());
    }
    
}


package mainfatura;


public class Fatura {
     private String numeroItem;
    private String descricaoItem;
    private int quantidade;
    private double precoUnitario;

    // Construtor
    public Fatura(String numeroItem, String descricaoItem, int quantidade, double precoUnitario) {
        this.numeroItem = numeroItem;
        this.descricaoItem = descricaoItem;
        // Verifica se a quantidade é positiva, senão configura como 0
        if (quantidade > 0)
            this.quantidade = quantidade;
        else
            this.quantidade = 0;
        // Verifica se o preço unitário é positivo, senão configura como 0.0
        if (precoUnitario > 0.0)
            this.precoUnitario = precoUnitario;
        else
            this.precoUnitario = 0.0;
    }

    // Métodos get e set para cada atributo
    public String getNumeroItem() {
        return numeroItem;
    }

    public void setNumeroItem(String numeroItem) {
        this.numeroItem = numeroItem;
    }

    public String getDescricaoItem() {
        return descricaoItem;
    }

    public void setDescricaoItem(String descricaoItem) {
        this.descricaoItem = descricaoItem;
    }

    public int getQuantidade() {
        return quantidade;
    }

    public void setQuantidade(int quantidade) {
        if (quantidade > 0)
            this.quantidade = quantidade;
        else
            this.quantidade = 0;
    }

    public double getPrecoUnitario() {
        return precoUnitario;
    }

    public void setPrecoUnitario(double precoUnitario) {
        if (precoUnitario > 0.0)
            this.precoUnitario = precoUnitario;
        else
            this.precoUnitario = 0.0;
    }

    // Método para calcular o valor da fatura
    public double getValorDaFatura() {
        return quantidade * precoUnitario;
    }
    
}
