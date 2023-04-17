# Ordenando-valores-do-vetor-java
Ordenando as variaveis do vetor java usando interface

// interface
public interface vouordernaaqui {
    void swap(int vet[]);
}
//preenchendo o metodo da interface

package ordenacaovetor;


public class metodos implements vouordernaaqui{

 

    @Override
    public void swap(int vet[]){
        int aux = 0;
        boolean controle = true;
        
           for (int i = 0; i < vet.length; i++)
        {
         for(int j = 0; j < (vet.length); j++) {
         if(vet[i] < vet[j]) {

             aux = vet[i];
             vet[i] = vet[j];
             vet[j] = aux;
         }

      }  
   }
    for(int i = 0; i < vet.length; i++) 
        System.out.println(vet[i] + "");
}

      }
      
      // metodo main
      public class Ordenacaovetor {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        Scanner teclado = new Scanner(System.in);
        metodos m = new metodos();
        System.out.println("Quantods numeros deseja ordernar");
        int t = teclado.nextInt();
        int vet[] = new int [t];
        int controle = 0;
       int p = 0;
        

        while ( controle != -598){
     
            System.out.println("informe um numero");
            controle = teclado.nextInt();
            vet[p] = controle;
            
            if(p < t){
            p++;
            
            }
            if(p == t){
               controle = -598;
            }
        }
        System.out.println("Testado");
        
        m.swap(vet);
        
    }
    
}
