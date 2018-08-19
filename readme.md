## Workshop Steps
1. cucumber --init
2. สร้าง Gemfile เพื่อระบุ dependencies
3. รัน command เพื่อลง dependencies
```
bundle install
```
4. แก้ไข features/support/env.rb
```
require 'capybara/cucumber'
require 'selenium-webdriver'
require 'uri'

Capybara.default_driver = :selenium
```
เพื่อกำหนด lib และ driver สำหรับเปิด browser

5. โหลด geckodriver มา และแตก zip
https://github.com/mozilla/geckodriver/releases
ถ้าเป็น mac สามารถติดตั้งได้จาก brew install geckodriver ได้เลย

6. สร้าง feature / step definition
note. ถ้า error หา geckodriver ไม่เจอ .. ให้ย้าย geckodirver ไปที่ๆสามารถรัน globally ได้เช่น /usr/local/bin หรือจะเพิ่ม PATH environment variable ก็ได้
