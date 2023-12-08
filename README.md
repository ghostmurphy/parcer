# parcer
import requests
from bs4 import BeautifulSoup

url = "https://yandex.ru/pogoda/mytischi?lat=55.916489&lon=37.790798"
response = requests.get(url)

bs = BeautifulSoup(response.text, "html")

temp = bs.find('span', class_ = "weather__temp")
print(temp)

