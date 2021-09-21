# DesignPatterns
SOFE3650 Grp29


public interface Product{
void inventory ();
}


public class Product1 implements product {
@Override
public void inventory();
}


public class Product2 implements product {
@Override
public void inventory();
}



public class Product3 implements product {
@Override
public void inventory();
}


public abstract class AbstractFactory {
   abstract Product getProduct(String ProductType) ;
}



public class ProductFactory extends AbstractFactory {
   @Override
   public Product getProduct(String ProductType){    
      if(ProductType.equalsIgnoreCase("Product1")){
         return new product1();         
      }else if(ProductType.equalsIgnoreCase("Product2E")){
         return new product2();
      }	 
      return null;
   }
}
