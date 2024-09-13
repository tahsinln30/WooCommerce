// Registered User Place-Order Process


package Test;

import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;


public class Test {

	public static void main(String[] args) 
	
	{
		// TODO Auto-Generated Method Stub
		
		System.setProperty("webdriver.chrome.driver", "C:\\Users\\Hp\\eclipse-workspace\\Test\\Driver\\chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		
		// Screen Size 
		
		driver.manage().window().maximize();
		
		// Website URL
		
		driver.get("http://localhost/newsite");
		
		// Registered User
		
		// Log In Page

		driver.get("http://localhost/newsite/my-account/");
		
		// Auth Page
		
		   driver.findElement(By.id("username")).sendKeys("tahsin");
	       driver.findElement(By.id("password")).sendKeys("Admin@123");
	       driver.findElement(By.name("login")).click(); 
	       
	    // Shop Page   
	       
	       driver.get("http://localhost/newsite/shop");
	       
	    // Product Select, Add to Cart, Check-Out
	       
	       driver.get("http://localhost/newsite/product/funky-printed-black-bag/");
	       driver.findElement(By.name("add-to-cart")).click();  
	       
	       driver.get("http://localhost/newsite/cart/");
	       driver.get("http://localhost/newsite/checkout/");
	       
	    // Option Select
	   
	       driver.findElement(By.id("radio-control-wc-payment-method-options-cod")).click();
	       
	    // Place Order   
	       
	       driver.get("http://localhost/newsite/checkout/order-received/99/?key=wc_order_efapLIwjUTLwe");	
	       
	    // My Account
	       
	       driver.get("http://localhost/newsite/my-account/"); 
	       
	   //  Log Out and Auth Page
	       
	       driver.get("http://localhost/newsite/my-account/"); 
	       
//  Guest User
	       
	       driver.get("http://localhost/newsite/shop/");  
	       
      //   Product Select, Add to Cart, Check-Out
	       
	       driver.get("http://localhost/newsite/product/funky-printed-black-bag/");
	       driver.findElement(By.name("add-to-cart")).click();  
	       
	       driver.get("http://localhost/newsite/cart/");
	       driver.get("http://localhost/newsite/checkout/");
	       
	    // Option Select
	   
	       driver.findElement(By.id("radio-control-wc-payment-method-options-cod")).click();
	       
	    // Place Order   
	       
	       driver.get("http://localhost/newsite/checkout/order-received/99/?key=wc_order_efapLIwjUTLwe");	
	       
    }
	

}
