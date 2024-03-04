#My Prpoject - 1


package com;
import org.openqa.selenium.WebDriver;

import org.openqa.selenium.chrome.ChromeDriver;

import org.testng.annotations.AfterClass;

import org.testng.annotations.BeforeClass;

import org.testng.annotations.Test;
 
public class SeleniumTest {
 
    WebDriver driver;
 
    @BeforeClass
    public void setUp() {
        System.setProperty("webdriver.chrome.driver", "C:\\Users\\ranjit.gaikwad\\Downloads\\Ranjit\\Drivers\\chromedriver-win64\\chromedriver-win64");
        driver = new ChromeDriver();
    }
 
    @Test
    public void testGoogleSearch() {
        driver.get("https://www.google.com");
        System.out.println("Page title is: " + driver.getTitle());
    }
 
    @AfterClass
    public void tearDown() {
        driver.quit();
    }
}




