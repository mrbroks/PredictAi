# Stock Price Prediction Using LSTM | PredictAI

<img align="right" width="500px" src="/README%20static/89927%20%5BConverted%5D.png" />

<p align="left">
Accurate stock price prediction is challenging due to the volatile and non-linear nature of the financial stock markets as it depends on various factors including but not limited to political conditions, the global economy, the company’s financial reports, and performance, etc.

In this graduation project, we created PredictAI a comprehensive stock price prediction platform designed to assist users in making informed financial decisions. PredictAI website stores historical stock prices for the last 5-20 years and employs the LSTM model to predict future prices based on past trends. The website's core feature leverages Long Short Term Memory (LSTM), a powerful deep learning model, to predict future stock price trends more accurately.
PredictAI's extensive database includes over 1,000+ top-performing NYSE-listed companies, offering real-time data on current stock prices. In addition to stocks, the platform provides live price charts for Bitcoin, Ethereum, and Gold (Oz), enabling users to monitor and assess multiple asset classes in one place.

By offering predictive insights and live market data, PredictAI empowers users to anticipate stock trends, thereby supporting more strategic financial investments.

You Can See Our Project on Behance: https://www.behance.net/gallery/209334735/PredictAI-Stock-Prediction-Project
</p>

Also, you can check our:-
- Graduation Report: https://drive.google.com/file/d/10BKp_fcMutuFxq5zblCxH2_Ho89l1u2f/view?usp=sharing
- Graduation Presentation: https://drive.google.com/file/d/19wGwl8NH9Vh10CLAS5cFjYO6aExDumlI/view?usp=sharing

### Technologies used 
- Python
- Flask
- JavaScript
- HTML & CSS
- MSSQL & SQLAlchemy
- Git

### Key Features Summary
- Store historical stock prices for more than 1000+ companies for the past 5-20 years.
- Use LSTM time series model for future price forecasting.
- Include TradingView API for current stock prices.
- Secure & encrypted user account registration.
- Implemented ORM with SQLAlchemy for Database Management; added indexing for performance.
- Implemented data integration scripts (CSV downloading and merging).


<br/>


## Installation
#### Note: Make sure Python 3.9 or above is installed.

1. Import ```StockAI.bacbak``` file as a data-tier application in MSSQL, you can download the database from here(104 Mb): https://drive.google.com/file/d/1XBKmLDz95M4pqBY0DKnrvpldgsYH1tET/view?usp=sharing
2. Install python libraries
```bash
  pip install Requirements.txt
```
#### If it doesn't work try
```bash
  py -m pip install Requirements.txt
```
3. In ```__init__.py``` file change ```SERVER_NAME = 'DESKTOP-329F25T'``` to your MSSQL server name and make sure that ```DATABASE_NAME = 'StockAI'```.
4. Run ```run.py``` file like a normal Python file.
5. Follow the link in the terminal or paste this link into the browser tab ```http://127.0.0.1:5000```. 


<br/>


## Some problems we faced and how we overcame them
We faced many bugs and problems while working on the project, problems that consumed big time and effort, here are a few of the most significant problems that we faced and how we solved them: 
 - In the prediction code we faced a problem when we tried to get stock prices from the Database and fetch them into the LSTM Model, the problem was that we wanted ```Close``` price but when we got it from the database it gave the price and its data type 'float64' and to fix this we stored the close prices in temporary CSV files ```Company_ Validate.csv```, and ```Company_Train.csv```.
 - The website takes so much time to load due to yfinance API having many companies to load their current prices and we fixed that by putting all the companies into one list and running ```ThreadPoolExecutor()``` function to manage thread pools and prevent deadlocks therefore running them in a parallel instead of a serial processing.
 - The stock prediction page requires too much time to load due to the query of the available 900 companies from the database and we fixed that by adding pagination at the end of the page to make each page have 50 companies only and that made a huge difference in the loading time of the page.
 - We had a major problem because when we wanted to update the database with the new prices it would take so much time because we have 900 companies and we have to download each one manually so we fixed that by creating scripts that download all the 900 companies data at once from yahoo finance historical data then we made another python script to combine the 900 companies' data into one CSV then insert this CSV data into the database table Company.


<br/>


## Project Images
<p align="center"><img src="/README%20static/1.png" width="900" style="margin:100px ></p>
<p align="center"><img src="/README%20static/2.png" width="900" style="margin:100px ></p>
<p align="center"><img src="/README%20static/3.png" width="900" style="margin:100px ></p>
<p align="center"><img src="/README%20static/4.png" width="900" style="margin:100px ></p>
<p align="center"><img src="/README%20static/5.png" width="900" style="margin:100px ></p>
<p align="center"><img src="/README%20static/6.png" width="900" style="margin:100px ></p>
<p align="center"><img src="/README%20static/7.png" width="900" style="margin:100px ></p>
<p align="center"><img src="/README%20static/8.png" width="900" style="margin:100px ></p>
<p align="center"><img src="/README%20static/9.png" width="900" style="margin:100px ></p>
<p align="center"><img src="/README%20static/10.png" width="900" style="margin:100px ></p>
<p align="center"><img src="/README%20static/11.png" width="900" style="margin:100px ></p>
<p align="center"><img src="/README%20static/12.png" width="900" style="margin:100px ></p>
<p align="center"><img src="/README%20static/13.png" width="900" style="margin:100px ></p>
<p align="center"><img src="/README%20static/14.png" width="900" style="margin:100px ></p>
<p align="center"><img src="/README%20static/17.png" width="900" style="margin:100px ></p>
<p align="center"><img src="/README%20static/18.png" width="900" style="margin:100px ></p>
<p align="center"><img src="/README%20static/19.png" width="900" style="margin:100px ></p>
<p align="center"><img src="/README%20static/20.png" width="900" style="margin:100px ></p>
<p align="center"><img src="/README%20static/21.png" width="900" style="margin:100px" ></p>


<br/>


## Our Team
- [Mohammed Hisham](https://github.com/mrbroks)
- [Marco George](https://github.com/Marcogeorgez)


<br/>


## Colors Used
| Hex                                                                |
| ------------------------------------------------------------------ |
| ![](https://via.placeholder.com/10/5f4be2?text=+) #5f4be2 |
| ![](https://via.placeholder.com/10/21222C?text=+) #21222C |
| ![](https://via.placeholder.com/10/131315?text=+) #131315 |
| ![](https://via.placeholder.com/10/FDFAFF?text=+) #FDFAFF |
| ![](https://via.placeholder.com/10/E8E8F7?text=+) #E8E8F7 |
| ![](https://via.placeholder.com/10/E3E6F7?text=+) #E3E6F7 |
| ![](https://via.placeholder.com/10/26272B?text=+) #26272B |
| ![](https://via.placeholder.com/10/D33636?text=+) #D33636 |
| ![](https://via.placeholder.com/10/58BC7D?text=+) #58BC7D |

