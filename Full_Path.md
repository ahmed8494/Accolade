package mytest;

import java.util.concurrent.TimeUnit;

import org.openqa.selenium.By;
import org.openqa.selenium.Keys;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.interactions.Actions;
import org.openqa.selenium.support.ui.ExpectedConditions;
import org.openqa.selenium.support.ui.Select;
import org.openqa.selenium.support.ui.WebDriverWait;

public class AccoladeFullPath {

	public static void main(String[] args) throws InterruptedException {
		// TODO Auto-generated method stub
		System.setProperty("webdriver.chrome.driver", "C:\\Users\\577503\\Downloads\\Selenium Apps\\chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.manage().deleteAllCookies();
		driver.manage().window().maximize();
		driver.manage().timeouts().implicitlyWait(5, TimeUnit.SECONDS);

		driver.get("https://lolg2gtest.sopheon.com");

		driver.findElement(By.className("largeIcon")).click();
		driver.findElement(By.linkText("Project")).click();
		Actions builder = new Actions(driver);
		WebElement element = driver.findElement(By.linkText("Add New"));
		builder.moveToElement(element).build().perform();

		WebElement element1 = driver.findElement(By.linkText("G2G2 Full Path"));
		builder.moveToElement(element1).click().perform();

		driver.findElement(By.xpath("//button[@class='buttonStandard user-select-btn']")).click();

		Select user = new Select(driver.findElement(By.xpath("//select[@id='userResultsSelect']")));
		user.selectByVisibleText("Ahmed Zaman");
		driver.findElement(By.xpath("//span[text()='Done']")).click();
		driver.findElement(By.xpath("//input[@id='ProjectName']")).sendKeys("Ahmed_Full Path SE");
		driver.findElement(By.xpath("//textarea[@id='ProjectDescription']")).sendKeys("To Test Auto for Full Path");

		driver.findElement(By.xpath("//div[@title='Lead Business Unit']/div")).click();
		driver.findElement(By.xpath("//option[@value='FoodService']")).click();

		driver.findElement(By.xpath("//div[@title='Other Impacted Business Units']/div")).click();
		driver.findElement(By.xpath("//option[@value='Retail']")).click();

		driver.findElement(By.xpath("//div[@title='R&D Platform']/div")).click();
		driver.findElement(By.xpath("//option[@value='Emerging']")).click();

		driver.findElement(By.xpath("//div[@title='Lead Sub Business Unit']/div")).click();
		driver.findElement(By.xpath("//option[@value='Foodservice Kozy']")).click();

		driver.findElement(By.xpath("//div[@title='Portfolio Type New']/div")).click();
		driver.findElement(By.xpath("//option[@value='Exploratory']")).click();

		driver.findElement(By.xpath("//div[@title='Project Type New']/div")).click();
		driver.findElement(By.xpath("//option[@value='Emerging Technologies']")).click();

		driver.findElement(By.xpath("//button[@id='BtnCreateProject']")).click();

		Select status = new Select(driver.findElement(By.xpath("(//select[@class='quickgridControl'])[3]")));
		status.selectByValue("Green");

		driver.findElement(By.xpath("//input[@class='hasDatepicker quickgridControl']")).click();
		driver.findElement(By.xpath("//*[text()='15']")).click();

		Select plant1 = new Select(driver.findElement(By.xpath("(//select[@class='quickgridControl'])[8]")));
		plant1.selectByValue("Carlisle");

		Select plant2 = new Select(driver.findElement(By.xpath("(//select[@class='quickgridControl'])[9]")));
		plant2.selectByValue("AMPI");

		driver.findElement(By.xpath("//div[@class='quickGridRenderInnerContainer  ']")).click();

		WebDriverWait close9 = new WebDriverWait(driver, 10);
		close9.until(ExpectedConditions.elementToBeClickable(By.xpath("(//button[text()='Apply'])[1]")));
		driver.findElement(By.xpath("(//button[text()='Apply'])[1]")).click();

		driver.findElement(By.xpath("//div[@data-qme='1945']")).sendKeys(Keys.ENTER, " -Test 123");
		driver.findElement(By.xpath("//div[@data-qme='1905']")).sendKeys(Keys.ENTER, " -Test 123");
		driver.findElement(By.xpath("//div[@data-qme='1856']")).sendKeys(Keys.ENTER, " -Test 123");

		Select role = new Select(driver.findElement(By.xpath("(//select[@class='quickgridControl'])[10]")));
		role.selectByValue("Grow");

		driver.findElement(By.xpath("//div[@data-qme='1312']")).sendKeys(Keys.ENTER, " -Test 123");
		driver.findElement(By.xpath("//div[@data-qme='1872']")).sendKeys(Keys.ENTER, " -Test 123");
		driver.findElement(By.xpath("//div[@data-qme='1903']")).sendKeys(Keys.ENTER, " -Test 123");
		driver.findElement(By.xpath("//div[@data-qme='1854']")).sendKeys(Keys.ENTER, " -Test 123");
		driver.findElement(By.xpath("//div[@data-qme='1857']")).sendKeys(Keys.ENTER, " -Test 123");

		WebDriverWait wait = new WebDriverWait(driver, 20);
		wait.until(ExpectedConditions.visibilityOfElementLocated(By.xpath("(//button[text()='Apply'])[2]")));
		driver.findElement(By.xpath("(//td[@class='quickGridGridTitle'])[2]")).click();

		driver.findElement(By.xpath("(//button[@class='apply buttonPrimary cursorPointer'])[2]")).click();
		Thread.sleep(3000);

		WebDriverWait wait2 = new WebDriverWait(driver, 10);
		wait2.until(ExpectedConditions.elementToBeClickable(
				By.xpath("//div[contains(@class,'projectNavPoleLabel')][contains(text(),'2 - Risks')]")));
		driver.findElement(By.xpath("//div[contains(@class,'projectNavPoleLabel')][contains(text(),'2 - Risks')]"))
				.click();

		driver.findElement(By.xpath("(//button[text()='Add New Row'])[1]")).click();

		driver.findElement(By.xpath("(//div[@data-qme='1917'])[2]")).click();
		driver.findElement(By.xpath("//div[@role='dialog']/textarea")).sendKeys("Test the Risk");
		driver.findElement(By.xpath("(//span[text()='OK'])[2]")).click();

		driver.findElement(By.xpath("(//div[@data-qme='1921'])[2]")).click();
		driver.findElement(By.xpath("//div[@role='dialog']/textarea")).sendKeys("Test the Risk");
		driver.findElement(By.xpath("(//span[text()='OK'])[2]")).click();

		Select likelihood = new Select(driver.findElement(By.xpath("(//select[@class='quickgridControl'])[1]")));
		likelihood.selectByValue("3 Likely 50%-75%");

		Select severity = new Select(driver.findElement(By.xpath("(//select[@class='quickgridControl'])[2]")));
		severity.selectByValue("3 High");

		driver.findElement(By.xpath("(//div[@data-qme='1931'])[2]")).click();
		driver.findElement(By.xpath("//div[@role='dialog']/textarea")).sendKeys("Test the Risk");
		driver.findElement(By.xpath("(//span[text()='OK'])[2]")).click();

		Select response = new Select(driver.findElement(By.xpath("(//select[@class='quickgridControl'])[3]")));
		response.selectByValue("Yes");

		driver.findElement(By.xpath("//input[@class='hasDatepicker quickgridControl']")).click();
		driver.findElement(By.xpath("//*[text()='15']")).click();

		driver.findElement(By.xpath("//button[@class='apply buttonPrimary cursorPointer']")).click();
		Thread.sleep(3000);

		driver.findElement(By.xpath("//div[text()='4 - Decision']")).click();

		driver.findElement(By.xpath("//div[@data-qme='1317']")).click();
		driver.findElement(By.xpath("//textarea[@class='quickgridControl']")).sendKeys("Test the Risk");
		driver.findElement(By.xpath("(//span[text()='OK'])[2]")).click();

		Select decision = new Select(driver.findElement(By.xpath("(//select[@class='quickgridControl'])[1]")));
		decision.selectByValue("Go");

		driver.findElement(By.xpath("//div[@data-qme='1974']")).click();
		driver.findElement(By.xpath("//textarea[@class='quickgridControl']")).sendKeys("Test the Risk");
		driver.findElement(By.xpath("(//span[text()='OK'])[2]")).click();

		driver.findElement(By.xpath("//div[@data-qme='1916']")).click();
		driver.findElement(By.xpath("//textarea[@class='quickgridControl']")).sendKeys("Test the Risk");
		driver.findElement(By.xpath("(//span[text()='OK'])[2]")).click();

		driver.findElement(By.xpath("//div[@data-qme='1915']")).click();
		driver.findElement(By.xpath("//textarea[@class='quickgridControl']")).sendKeys("Test the Risk");
		driver.findElement(By.xpath("(//span[text()='OK'])[2]")).click();

		driver.findElement(By.xpath("//button[@class='apply buttonPrimary cursorPointer']")).click();
		Thread.sleep(3000);

		WebDriverWait close6 = new WebDriverWait(driver, 10);
		close6.until(ExpectedConditions.elementToBeClickable(By.xpath("//div[text()='5 - Lesson Learned']")));

		driver.findElement(By.xpath("//div[text()='5 - Lesson Learned']")).click();

		driver.findElement(By.xpath("//div[@data-qme='2048']")).sendKeys(Keys.ENTER, " -Test 123");
		driver.findElement(By.xpath("//div[@data-qme='2049']")).sendKeys(Keys.ENTER, " -Test 123");
		driver.findElement(By.xpath("//div[@data-qme='2050']")).sendKeys(Keys.ENTER, " -Test 123");

		driver.findElement(By.xpath("//input[@class='hasDatepicker quickgridControl']")).click();
		driver.findElement(By.xpath("//*[text()='15']")).click();

		driver.findElement(By.xpath("//button[@id='LayoutApply']")).click();

		Thread.sleep(3000);
		driver.findElement(By.xpath("//div[text()='Stages']")).click();

		driver.findElement(By.xpath("//div[@class='linkWithImageText']")).click();

		driver.findElement(By.xpath("//button[@class='apply buttonPrimary cursorPointer']")).click();

		Thread.sleep(3000);
		driver.findElement(By.xpath(
				"//div[@class='ui-dialog-titlebar ui-widget-header ui-corner-all ui-helper-clearfix ui-draggable-handle']//button[@title='Close']"))
				.click();
	
		WebDriverWait close3 = new WebDriverWait(driver, 10);
		close3.until(ExpectedConditions.elementToBeClickable(By.xpath("//tr[@class='odd']/td[3]/div")));
		driver.findElement(By.xpath("//tr[@class='odd']/td[3]/div")).click();
		WebDriverWait close2 = new WebDriverWait(driver, 10);
		close2.until(ExpectedConditions.elementToBeClickable(By.xpath("(//option[@value='1'])[1]")));
		driver.findElement(By.xpath("(//option[@value='1'])[1]")).click();

		driver.findElement(By.xpath("//button[@id='Apply']")).click();

		driver.findElement(By.xpath("(//a[@class='subLabel gateDate dateEditor'])[1]")).click();
		
		WebDriverWait close1 = new WebDriverWait(driver, 10);
		close1.until(ExpectedConditions.elementToBeClickable(By.xpath("//a[text()='15']")));
		driver.findElement(By.xpath("//a[text()='15']")).click();

		driver.switchTo().alert().accept();

		driver.findElement(By.xpath("//div[@title='Manage Project Details']")).click();
		Thread.sleep(1000);
		driver.findElement(By.xpath("//li[text()='Close Project']")).click();

		driver.findElement(By.xpath("//textarea[@id='closeNotesText']")).sendKeys("Test");
		Thread.sleep(1000);
		driver.findElement(By.xpath("//button[@id='okbutton']")).click();

		System.out.println("Full path creation and close verified");
		driver.close();

	}

}
