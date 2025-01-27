# Scrapeless-Captcha-Solver-upgrade
WebUnlocker Improvements &amp; Serp API Now at $0.8/k
Data scraping is no longer optional but a must for many companies. Whether you are doing e-commerce, travel, or SEO analysis, the need to scrape web data is almost everywhere. However, CAPTCHA (verification code) often becomes the biggest obstacle in the scraping process. You may encounter such a situation: when scraping product information, a verification code suddenly pops up on the website, which makes the entire scraping process stagnant, and even requires additional payment to use a third-party verification code solution service. This not only wastes time, but also increases costs.
However, the problem is not just cost. The problem of verification code often brings operational complexity and inefficiency. You may have been accustomed to solving verification codes manually, or hiring a third-party verification code solution at a high cost. However, the result is often low efficiency of data scraping, unsmooth automation process, and even obstacles due to technical docking problems.

Today, we are happy to introduce the latest update of Scrapeless, which not only solves the verification code problem, but also greatly reduces the cost of scraping, making your scraping tasks smarter and more efficient. Next, we will explore in depth how these updates can help you better cope with challenges in actual work.

## 🚀 New feature of Scrapeless: Speed up your scraping
This Scrapeless feature upgrade can significantly speed up your web scraping tasks while maintaining high accuracy. Whether you are scraping large amounts of data or working on time-sensitive projects, this upgrade can help you get results more efficiently, resulting in a smoother and faster workflow.
### Upgrade 1: Optimized Captcha automatic solution: verification code is no longer an obstacle
When it comes to data scraping, one of the biggest problems is CAPTCHA (verification code). Many websites use verification codes to prevent robots from crawling data, however, this also brings troubles to us legitimate data scrapers.

**Do you often encounter the following problems:**
- When you encounter verification codes frequently, your crawling tasks will be interrupted or even stagnant.
- Some verification code recognition tools require additional payment, and technically cannot solve all types of verification codes 100%.
- If you solve verification codes manually, the data crawling process will be seriously slowed down.

The latest optimization of Scrapeless allows our Captcha automatic solver to fix the verification code recognition problem in the [Scraping browser](https://www.scrapeless.com/en/product/scraping-browser?utm_source=official&utm_medium=blog&utm_campaign=productupgrade), solving the problem that the requested site cannot be accessed because the verification code cannot be recognized or recognized incorrectly.

**What can you benefit from this update?**

- Seamless scraping: Whether you are scraping e-commerce data, flight information, or hotel data, Scrapeless can help you easily bypass CAPTCHA and continue to scrape data.
- 100% free: Unlike many competitors that charge extra, Scrapeless's captcha solver is already included and is completely free! This not only simplifies your scraping process, but also greatly reduces costs, helping you save money on purchasing third-party captcha solutions.

### Upgrade 2: CDP API Update: Make Automation Smoother
Many users have reported that in the automation process, the appearance of verification codes often requires manual intervention, which seriously affects work efficiency. When they want to integrate the verification code solving process into the automation tool, many tools require complex technical configuration and are not stable.

**Don't worry now, because:**

The new features of Scrapeless are not only to improve the success rate of crawling, but also upgrade the CDP API. Now, Scrapeless can allow you to directly receive verification code tokens in the automated crawling process through the Captcha Solved callback event. This means that you can directly integrate verification code solving through automation tools such as Puppeteer, simplifying the workflow and improving efficiency.

**What benefits can this update bring to you?**
- More efficient automation process: You no longer need to solve the verification code manually. Through the callback event, your automation process can continue to move forward, saving valuable time.
- Smoother integration: The callback event can be triggered directly in your automation tool, without manual intervention, making the crawling task more efficient.

### Upgrade 3: SERP API price reduction: faster and cheaper

High API fees make scraping costs unaffordable, especially when scraping large amounts of data. Scrapeless not only provides optimizations in CAPTCHA solving, but also pays attention to this user problem in a timely manner. Scrapeless's SERP API price has also dropped to only $0.8 per thousand queries (compared to many competitors in the industry, our price is 10 times cheaper), making Scrapeless the cheapest and fastest scraping solution on the market.

> Users who need to frequently query search engine results are often constrained by high-priced API providers, which affects crawling efficiency. **Scrapeless Serp API is now only $0.8/k**.
> 
> You can also apply for a free trial. [Click](https://app.scrapeless.com/passport/login?utm_source=official&utm_medium=blog&utm_campaign=productupgrade) now to get a free trial opportunity!

***User reviews:***
In general, Scrapeless is a very efficient crawling tool that can help businesses of all sizes solve data extraction problems. It is fast and powerful, making it an ideal choice for e-commerce, market research, SEO analysis and other fields. - <a href="https://slashdot.org/software/p/Scrapeless/#reviews" rel="nofollow"><strong>Users</strong></a>

## 🛠️ Practical features brought by Scrapeless

### 1. Free Captcha solving function

We know that many scraping tools require you to pay extra to use third-party Captcha solving services, which puts a lot of pressure on companies with limited budgets. Unlike other tools, **Scrapeless's built-in Captcha solving** function in our [Scraping Browser](https://www.scrapeless.com/en/product/scraping-browser?utm_source=official&utm_medium=blog&utm_campaign=productupgrade) and [Web Unlocker](https://www.scrapeless.com/en/product/web-unlocker?utm_source=official&utm_medium=blog&utm_campaign=productupgrade) is ***completely free*** and does not require additional purchase.

**Main Features:**
- Save additional CAPTCHA solving costs
- Simplify tool docking, no need to dock with third-party verification code services
- Efficiently solve **reCaptcha v2 (5-8 seconds) and reCaptcha v3 (0-4 seconds)** verification codes with an accuracy rate of **more than 95%**
### 2. Faster verification code recognition and higher accuracy

With the advancement of technology, [Scrapeless's Captcha Solver](https://www.scrapeless.com/en/product/captcha-solver?utm_source=official&utm_medium=blog&utm_campaign=productupgrade) has been able to solve various verification codes at extremely high speed and accuracy, especially the recognition ability of reCaptcha v2 and reCaptcha v3 has reached an accuracy rate of more than 95%.


**We also specifically fixed the following issues:**
- **reCaptcha nesting issue:** We fixed a problem where pages were nested and the CAPTCHA was not recognized, especially on some specific sites.
- **Turnstile challenge issue:** Previously, our solver would incorrectly identify it as a Cloudflare challenge, which is now fixed.

**Implementation Example - Captcha Solver**

Node.js（Puppeteer）
```
// Listen for CAPTCHA solving events
const client = await page.createCDPSession();

client.on('Captcha.detected', (result) => {
  console.log('Captcha detected:', result);
});

await new Promise((resolve, reject) => {
  client.on('Captcha.solveFinished', (result) => {
    if (result.success) resolve();
  });
  client.on('Captcha.solveFailed', () =>
    reject(new Error('Captcha solve failed'))
  );
  setTimeout(() =>
      reject(new Error('Captcha solve timeout')),
    5 * 60 * 1000
  );
});

```
Python(Playwright)
```
page = await browser.contexts[0].new_page()
client = await page.context.new_cdp_session(page)

client.on('Captcha.detected', lambda c: print('Captcha detected:', c))
client.on('Captcha.solveFinished', lambda _: print('Captcha solved!'))
client.on('Captcha.solveFailed', lambda _: print('Captcha failed!'))

```
## 👥 How does Scrapeless provide solutions for different industries?
Scrapeless is not just a simple data scraping tool, it can help companies in e-commerce, tourism, SEO and other industries solve specific scraping problems.
### 1. E-commerce industry
Data capture on e-commerce platforms is often hindered by verification codes. E-commerce companies need to monitor competitor prices and capture product information, and [Scrapeless Captcha Solver](https://www.scrapeless.com/en/product/captcha-solver?utm_source=official&utm_medium=blog&utm_campaign=productupgrade) can provide accurate identification and fast response, ensuring an accuracy rate of more than 95%, providing e-commerce companies with sustainable competitiveness.
### 2. Tourism Industry
Travel companies often need to scrape information such as flights and hotels, and many travel websites use CAPTCHA to prevent data scraping. With Scrapeless, travel companies can easily break through these verification codes and quickly obtain the latest market data. In addition, Scrapeless also provides a powerful [Google Flights Scraping API](https://www.scrapeless.com/en/blog/google-flights-scraper?utm_source=official&utm_medium=blog&utm_campaign=productupgrade) to help companies scrape flight information in real time and improve decision-making efficiency. You can visit [Scrapeless's API completion documentation](https://apidocs.scrapeless.com/api-11949851?utm_source=official&utm_medium=blog&utm_campaign=productupgrade) for detailed information.
### 3.SEO Industry
SEO analysts and marketers rely on search engine data to track rankings, analyze competitors, and more. [Scrapeless SERP API](https://www.scrapeless.com/en/product/scraping-api?utm_source=official&utm_medium=blog&utm_campaign=productupgrade) helps them efficiently collect data from search engine results pages (SERPs) without having to worry about interference caused by verification codes. At the same time, Scrapeless also provides [Google Trends API](https://www.scrapeless.com/en/solutions/google-trends?utm_source=official&utm_medium=blog&utm_campaign=productupgrade), which enables users to dig deep into trend data and analyze keyword popularity and market dynamics. This combination not only improves the efficiency of data collection, but also provides a more accurate basis for the formulation of marketing strategies, helping companies stay ahead in the highly competitive market.
## 🎯 Conclusion
Whether you are an e-commerce seller, travel agent, or SEO expert, Scrapeless can provide an efficient, reliable, and low-cost solution for your data scraping tasks. If you are looking for a tool that can improve the success rate of scraping and reduce costs, Scrapeless is your best choice!
> 🎉 Join the weekly [product feedback event](https://discord.com/invite/xBcTfGPjCQ?utm_source=official&utm_medium=blog&utm_campaign=productupgrade)
Share your feedback every Friday to Sunday and get $10 credit!
