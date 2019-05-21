# datasource/GBIF
Uses [Registry API](https://www.gbif.org/developer/registry)

* current test uses: http://api.gbif.org/v1/dataset/search?country=TW, with resulting in [440 datasets](https://github.com/imaptwlife/datasource/blob/master/gbif-twdatasets-20190518.csv)
  * note many datasets, including TaiwanBBS, eBird, twMoth, are not detected by this API
  * a further test with http://api.gbif.org/v1/dataset/search?type=SAMPLING_EVENT&country=TW is even worse, which results in 0 dataset
  * However http://api.gbif.org/v1/dataset/search?publishingCountry=TW resulting in 53 datasest does includes TaiwanBBS and twMoth
  * and http://api.gbif.org/v1/dataset/search?type=SAMPLING_EVENT&publishingCountry=TW gets 6 dataset that does include TaiwanBBS...

* To create the potential list of GBIF datasets to compile into TBN
  * 先用第一個API "http://api.gbif.org/v1/dataset/search?country=TW" 所抓出的440個當基底
  * 確認資料筆數超過10,000筆以上的有沒有都在440個裡面，兩個取聯集後的資料集清單作為要以API抓資料進TBN的清單。
