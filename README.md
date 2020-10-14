 # How to download Kaggle dataset in colab.



```python
!pip install kaggle
```

    Requirement already satisfied: kaggle in /usr/local/lib/python3.6/dist-packages (1.5.8)
    Requirement already satisfied: python-dateutil in /usr/local/lib/python3.6/dist-packages (from kaggle) (2.8.1)
    Requirement already satisfied: tqdm in /usr/local/lib/python3.6/dist-packages (from kaggle) (4.41.1)
    Requirement already satisfied: six>=1.10 in /usr/local/lib/python3.6/dist-packages (from kaggle) (1.15.0)
    Requirement already satisfied: requests in /usr/local/lib/python3.6/dist-packages (from kaggle) (2.23.0)
    Requirement already satisfied: urllib3<1.25,>=1.21.1 in /usr/local/lib/python3.6/dist-packages (from kaggle) (1.24.3)
    Requirement already satisfied: certifi in /usr/local/lib/python3.6/dist-packages (from kaggle) (2020.6.20)
    Requirement already satisfied: python-slugify in /usr/local/lib/python3.6/dist-packages (from kaggle) (4.0.1)
    Requirement already satisfied: slugify in /usr/local/lib/python3.6/dist-packages (from kaggle) (0.0.1)
    Requirement already satisfied: chardet<4,>=3.0.2 in /usr/local/lib/python3.6/dist-packages (from requests->kaggle) (3.0.4)
    Requirement already satisfied: idna<3,>=2.5 in /usr/local/lib/python3.6/dist-packages (from requests->kaggle) (2.10)
    Requirement already satisfied: text-unidecode>=1.3 in /usr/local/lib/python3.6/dist-packages (from python-slugify->kaggle) (1.3)
    

![](https://miro.medium.com/max/875/1*f94G6dXm-8cRxX5FFTCqyg.png)

![](https://miro.medium.com/max/875/1*rhsGKThdgxwUoskaACSlwA.png)


```python
!mkdir ~/.kaggle
```


```python
# upload kaggle.json file in colab directly
!cp kaggle.json ~/.kaggle/
```


```python
!chmod 600 ~/.kaggle/kaggle.json
```


```python
!kaggle datasets list
```

    Warning: Looks like you're using an outdated API Version, please consider updating (server 1.5.6 / client 1.5.4)
    ref                                                               title                                                 size  lastUpdated          downloadCount  
    ----------------------------------------------------------------  --------------------------------------------------  ------  -------------------  -------------  
    christianlillelund/donald-trumps-rallies                          Donald Trump's Rallies                               720KB  2020-09-26 10:25:08            672  
    heeraldedhia/groceries-dataset                                    Groceries dataset                                    257KB  2020-09-17 04:36:08           3216  
    andrewmvd/trip-advisor-hotel-reviews                              Trip Advisor Hotel Reviews                             5MB  2020-09-30 08:31:20           1842  
    balraj98/stanford-background-dataset                              Stanford Background Dataset                           17MB  2020-09-26 12:57:59            192  
    nehaprabhavalkar/indian-food-101                                  Indian Food 101                                        7KB  2020-09-30 06:23:43           2590  
    jilkothari/finance-accounting-courses-udemy-13k-course            Finance & Accounting Courses - Udemy (13K+ course)  1000KB  2020-09-17 12:46:12            890  
    balraj98/massachusetts-roads-dataset                              Massachusetts Roads Dataset                            6GB  2020-09-26 03:57:49            159  
    arslanali4343/top-personality-dataset                             Top Personality Dataset                                9MB  2020-09-27 21:25:45            985  
    oldaandozerskaya/fiction-corpus-for-agebased-text-classification  RusAge: Corpus for Age-Based Text Classification     509MB  2020-09-28 09:30:12             63  
    gpreda/chinese-mnist                                              Chinese MNIST                                         10MB  2020-08-05 12:36:00            326  
    gpreda/local-elections-romania-2020                               Local Elections Romania 2020                          28MB  2020-09-27 20:46:11            161  
    anth7310/mental-health-in-the-tech-industry                       Mental Health in the Tech Industry                     2MB  2020-09-27 11:17:23           1422  
    roshansharma/sanfranciso-crime-dataset                            Sanfranciso Crime Dataset                              6MB  2019-05-29 12:45:44           4187  
    bppuneethpai/tldr-summary-for-man-pages                           TLDR summary for man pages                             8MB  2020-09-25 09:50:10             34  
    sterby/german-recipes-dataset                                     German Recipes Dataset                                 5MB  2019-03-06 16:25:22            900  
    arslanali4343/real-estate-dataset                                 Real Estate DataSet                                   12KB  2020-09-28 21:25:33           1132  
    thomaskonstantin/top-270-rated-computer-science-programing-books  Top 270 Computer Science / Programing Books           45KB  2020-09-28 16:47:12            536  
    leangab/poe-short-stories-corpuscsv                               E.A. Poe's corpus of short stories                   725KB  2020-09-28 11:43:08            118  
    anmolkumar/health-insurance-cross-sell-prediction                 Health Insurance Cross Sell Prediction 🏠 🏥             6MB  2020-09-11 18:39:31           4489  
    ramjidoolla/ipl-data-set                                          IPL _Data_Set                                          1MB  2020-09-14 10:57:42           4437  
    


```python
!kaggle competitions list
```

    Warning: Looks like you're using an outdated API Version, please consider updating (server 1.5.6 / client 1.5.4)
    ref                                            deadline             category            reward  teamCount  userHasEntered  
    ---------------------------------------------  -------------------  ---------------  ---------  ---------  --------------  
    contradictory-my-dear-watson                   2030-07-01 23:59:00  Getting Started     Prizes        224           False  
    gan-getting-started                            2030-07-01 23:59:00  Getting Started     Prizes        160           False  
    tpu-getting-started                            2030-06-03 23:59:00  Getting Started  Knowledge        359           False  
    digit-recognizer                               2030-01-01 00:00:00  Getting Started  Knowledge       2427            True  
    titanic                                        2030-01-01 00:00:00  Getting Started  Knowledge      17889            True  
    house-prices-advanced-regression-techniques    2030-01-01 00:00:00  Getting Started  Knowledge       4650            True  
    connectx                                       2030-01-01 00:00:00  Getting Started  Knowledge        416            True  
    nlp-getting-started                            2030-01-01 00:00:00  Getting Started  Knowledge       1195           False  
    riiid-test-answer-prediction                   2021-01-07 23:59:00  Featured          $100,000        674           False  
    competitive-data-science-predict-future-sales  2020-12-31 23:59:00  Playground           Kudos       9106            True  
    halite-iv-playground-edition                   2020-12-31 23:59:00  Playground       Knowledge         31           False  
    predict-volcanic-eruptions-ingv-oe             2020-12-28 23:59:00  Playground            Swag         38           False  
    hashcode-drone-delivery                        2020-12-14 23:59:00  Playground       Knowledge         62           False  
    cdp-unlocking-climate-solutions                2020-12-02 23:59:00  Analytics          $91,000          0           False  
    lish-moa                                       2020-11-30 23:59:00  Research           $30,000       2520           False  
    google-football                                2020-11-30 23:59:00  Featured            $6,000        662           False  
    conways-reverse-game-of-life-2020              2020-11-30 23:59:00  Playground            Swag        105           False  
    lyft-motion-prediction-autonomous-vehicles     2020-11-25 23:59:00  Featured           $30,000        616           False  
    rsna-str-pulmonary-embolism-detection          2020-10-26 23:59:00  Featured           $30,000        581            True  
    osic-pulmonary-fibrosis-progression            2020-10-06 23:59:00  Featured           $55,000       2097            True  
    


```python
!kaggle competitions download -c 'lish-moa'
```

    Warning: Looks like you're using an outdated API Version, please consider updating (server 1.5.6 / client 1.5.4)
    403 - Forbidden
    

# Create a directory named train,


```python
!mkdir train
```


# unzip train data there


```python
!unzip train.zip -d train
```

    unzip:  cannot find or open train.zip, train.zip.zip or train.zip.ZIP.
    

# For More help follow KaggleAPI Documentation
https://github.com/Kaggle/kaggle-api
