
import java.io.File;
import java.sql.Date;
import java.time.Duration;


import org.openqa.selenium.By;
import org.openqa.selenium.OutputType;
import org.openqa.selenium.TakesScreenshot;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.support.ui.Select;


public class sauce_demo {

	public static void main(String[] args) throws InterruptedException {
		
		 ChromeDriver driver = new ChromeDriver();
		 System.getProperty("webdriver.chrome.driver","C:\\Akilan\\chrome webdriver");
		 driver.get("https://www.saucedemo.com/");
		 driver.manage().timeouts().implicitlyWait(Duration.ofSeconds(20));
		 driver.findElement(By.xpath("//input[@placeholder='Username']")).sendKeys("standard_user");
		 driver.findElement(By.xpath("//input[@placeholder='Password']")).sendKeys("secret_sauc");
		 driver.findElement(By.xpath("//input[@id='login-button']")).click();
		 Thread.sleep(2000);
		 System.out.println(driver.findElement(By.cssSelector("h3[data-test='error']")).getText());
		 Thread.sleep(2000);
		 driver.findElement(By.xpath("//input[@placeholder='Password']")).clear();
		 Thread.sleep(2000);
		 driver.findElement(By.xpath("//input[@placeholder='Password']")).sendKeys("secret_sauce");
		 Thread.sleep(2000);
		 driver.findElement(By.xpath("//input[@id='login-button']")).click();
		 Thread.sleep(2000);
		 driver.findElement(By.id("react-burger-menu-btn")).click();
		 Thread.sleep(2000);
		 driver.findElement(By.id("react-burger-cross-btn")).click();
		 Thread.sleep(2000);
		 WebElement staticdropdown = driver.findElement(By.className("product_sort_container"));
         Select dropdown = new Select(staticdropdown);
         dropdown.selectByIndex(2);
         Thread.sleep(2000);
         driver.manage().window().maximize();
         Thread.sleep(2000);
         driver.findElement(By.id("add-to-cart-sauce-labs-bike-light")).click();
         Thread.sleep(2000);
         driver.findElement(By.className("shopping_cart_link")).click();
         Thread.sleep(2000);
         driver.findElement(By.id("checkout")).click();
         Thread.sleep(2000);
         driver.navigate().back();
         Thread.sleep(2000);
         driver.navigate().forward();
         Thread.sleep(2000);
         driver.findElement(By.xpath("//input[@placeholder='First Name']")).sendKeys("akilan");
         driver.findElement(By.xpath("//input[@placeholder='Last Name']")).sendKeys("M");
         driver.findElement(By.xpath("//input[@placeholder='Zip/Postal Code']")).sendKeys("akilanakl110@gmail.com");
         
         Thread.sleep(2000);
       
         Thread.sleep(2000);
         driver.findElement(By.id("continue")).click();
         System.out.println(driver.findElement(By.className("summary_total_label")).getText());
         Thread.sleep(2000);
         driver.findElement(By.id("react-burger-menu-btn")).click();
         Thread.sleep(2000);
         driver.findElement(By.id("logout_sidebar_link")).click();
		 
         

	}

}
