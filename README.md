## Automation of OTP-Based Login Verification Using Selenium WebDriver
### Name : Deepika S
### Reg:No: 212223230039

### CODE
```
from selenium import webdriver
from selenium.webdriver.common.by import By
import time
driver = webdriver.Chrome()
driver.get("https://www.flipkart.com/account/login")
driver.maximize_window()
mobile = input("Enter your mobile number: ")
mobile_box = driver.find_element(By.XPATH, "//input[@type='text' or @type='tel']")
mobile_box.send_keys(mobile)
time.sleep(1)
otp_button = driver.find_element(
    By.XPATH,
    "//button[contains(translate(., 'abcdefghijklmnopqrstuvwxyz', 'ABCDEFGHIJKLMNOPQRSTUVWXYZ'), 'REQUEST OTP')]"
)
otp_button.click()
print("OTP has been requested.")
otp = input("Enter the OTP received on your mobile: ")
otp_box = driver.find_element(By.XPATH, "//input[@type='text' or @type='tel']")
otp_box.send_keys(otp)
print("OTP entered.")
input("Press Enter to close...")
driver.quit()
```

### Output

<img width="1918" height="1000" alt="image" src="https://github.com/user-attachments/assets/0e50c572-f548-41ff-ba80-09d47cbd8a45" />


<img width="1918" height="897" alt="image" src="https://github.com/user-attachments/assets/0b02ea64-bd9a-473e-b47a-63176be40fdd" />


<img width="1918" height="1078" alt="image" src="https://github.com/user-attachments/assets/0948c9a3-a552-4478-bb61-4e6f3529d3b2" />


