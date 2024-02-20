import java.util.concurrent.TimeUnit;

import org.openqa.selenium.By;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.support.ui.Select;

public class FirstTest
{
	public static void main(String[] args)
	{
		System.setProperty("webdriver.chrome.driver", "D://SeleniumFiles/ChromeDrivers/ChromeDriver121.exe");
		
		ChromeDriver driver = new ChromeDriver();
		
		driver.get("https://katalon-demo-cura.herokuapp.com/");
		
		driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
		
		driver.manage().window().maximize();
		
		driver.findElement(By.linkText("Make Appointment")).click();
		
		driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
		
		driver.findElement(By.xpath("//*[@id='txt-username']")).sendKeys("John Doe");
		
		driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
		
		driver.findElement(By.xpath("//*[@id='txt-password']")).sendKeys("ThisIsNotAPassword");
		
		/*String text = driver.findElement(By.xpath("//*[@class='lead']")).getText();
		
		System.out.println(text);*/
		
		driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
		
		driver.findElement(By.xpath("//*[@id='btn-login']")).click();
		
		driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
		
		Select select = new Select(driver.findElement(By.xpath("//*[@id='combo_facility']")));
		select.selectByIndex(1);
		
		driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
		
		driver.findElement(By.xpath("//*[@id='chk_hospotal_readmission']")).click();
		
		driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
		
		driver.findElement(By.xpath("//*[@id='radio_program_medicaid']")).click();
		
		driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
		
		driver.findElement(By.xpath("//*[@id='txt_visit_date']")).sendKeys("31/03/2024");
		
		driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
		
		driver.findElement(By.xpath("//*[@id='btn-book-appointment']")).click();
		
		driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
		
		driver.findElement(By.xpath("//*[@class='btn btn-dark btn-lg toggle']")).click();
		
		driver.manage().timeouts().implicitlyWait(20, TimeUnit.SECONDS);
		
		driver.findElement(By.linkText("Logout")).click();
	}
}
