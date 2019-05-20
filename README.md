# datasource/GBIF
Uses [Registry API](https://www.gbif.org/developer/registry)

* current test uses: http://api.gbif.org/v1/dataset/search?country=TW, with resulting in [440 datasets](https://github.com/imaptwlife/datasource/blob/master/gbif-twdatasets-20190518.csv)
  * note many datasets, including TaiwanBBS, eBird, twMoth, are not detected by this API
  * a further test with http://api.gbif.org/v1/dataset/search?type=SAMPLING_EVENT&country=TW is even worse, which results in 0 dataset
  * also http://api.gbif.org/v1/dataset/search?publishingCountry=TW does not detect TaiwanBBS and twMoth
