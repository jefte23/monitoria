package monitoria;

import javax.swing.JOptionPane;

public class Array {

	public static void main(String[] args) {
		
		int lista [] = {1, 2, 3, 4, 5, 6};
		
		int tam = lista.length; // guarda o tamanho do array 'lista'
		int meio = 0; // guarda a quantidade de troca necessaria
		String ListaUm = "<<< Lista Original >>>" + "\n"+ " | ";
		String ListaDois = "<<< Lista Invertida >>>" + "\n"+ " | ";
		
		if (tam % 2 == 0) {
			meio = tam / 2;
		}else {
			meio = ((tam - 1) /2);
		}
		
		
		tam = tam - 1; // array começa na posição 0 logo a ultima posição é o tamanho - 1
		
		System.out.println("Tamaho: " +  tam);
		System.out.println("Meio: " +  meio);
		
		
		System.out.println("<<< Lista Original >>>");
		for (int i = 0; i < lista.length; i++) {
			System.out.println(lista[i]);
			ListaUm = ListaUm + lista[i] + " | ";
		}
		
		JOptionPane.showMessageDialog(null, ListaUm);
		

		for (int i = 0; i < meio; i++) {
				
			int temp = lista[i];
			lista[i] = lista[tam];
			lista[tam] = temp;
			
			tam = tam - 1;
		}

		System.out.println("<<< Lista Invertida >>>");
		for (int i = 0; i < lista.length; i++) {
			System.out.println(lista[i]);
			ListaDois = ListaDois + lista[i] + " | ";
		}
		JOptionPane.showMessageDialog(null, ListaDois);
	
	
	}
}
