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



public class Price extends AbstractFactory {
   @Override
   public Shape getProduct(String ProductType){    
      if(shapeType.equalsIgnoreCase("product1")){
         return new Price();         
      }else if(shapeType.equalsIgnoreCase("product2")){
         return new Pricee();
      }	 
      return null;
   }
}



public class FactoryProducer {
   public static AbstractFactory getFactory(boolean price){   
      if(price){
         return new Price();         
      }else{
         return new Product();
      }
   }
}



public class AbstractFactoryPattern {
   public static void main(String[] args) {
      //get product
      AbstractFactory Product = ProductProducer.getFactory(false);
      //get product1
      Product product1 = Product1Factory.getProduct("product1");
      //call inventory method of product1
      product1.inventory();
      //get product2 
      Product Product2 = ProductFactory.getProduct("product2");
      //call draw method product2
      Product2.draw();
     
      
      

      
      
      /
      
   }
}
