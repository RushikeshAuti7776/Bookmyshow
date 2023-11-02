import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.chrome.ChromeOptions;

public class BookmyshowAssignment {
	public static void main(String[] args) throws InterruptedException {
		ChromeOptions options = new ChromeOptions();
		 options.addArguments("--remote-allow-origins=*");
		System.setProperty("webdriver.chrome.driver","C:\\Software Testing\\chromedriver.exe");
		WebDriver driver = new ChromeDriver(options);
		driver.get("https://in.bookmyshow.com/explore/home/");
		driver.manage().window().maximize();
		
		
		Thread.sleep(1000);
		driver.findElement(By.xpath("//span[contains(text(),'Bengaluru')]")).click();
		driver.findElement(By.xpath("//div[contains(text(),'Sign in')]")).click();
		driver.findElement(By.xpath("//div[contains(text(),'Continue with Email')]")).click();
		
		driver.findElement(By.xpath("//*[@id=\"emailId\"]")).sendKeys("seleniumauto@yopmail.com");
		
		driver.findElement(By.xpath("//button[contains(text(),'Continue')]")).click();
		
		driver.get("https://yopmail.com/");
		
		driver.findElement(By.xpath("//input[@id='login']")).sendKeys("seleniumauto@yopmail.com");
		
		Thread.sleep(1000);
		
		driver.findElement(By.xpath("//*[@id=\"refreshbut\"]/button/i")).click();
	
	driver.navigate().refresh();
		
	//	driver.findElement(By.xpath("//*[@id=\"login\"]")).sendKeys("selauto@yopmail.com");
		
	//	Thread.sleep(2000);
	//	driver.findElement(By.xpath("//i[@class='material-icons-outlined f18 bhabs']")).click();
		
		
//		driver.navigate().back();	//	driver.findElement(By.xpath("")).click();
}
}//*[@id="login"]
