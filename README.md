A painstakingly collected data set for country info validation. I got quite tired of independent lists that needed reformatting and that did not have all the necessary info per data set.  This is the most comprehensive object json I am aware of.  I am going to be writing PHP/JS code for loading and quick data extraction but essentially all you need to do is download the JSON file (CountryData_minify.json) and load it in your scripts and your ready to go.

This data set merges several different independent datasets to create a single master country json object that can be used for HTML/Code validation when dealing with country specific information.

This object can be used to cross reference any country specific information for:
      Alpha2 code
      Alpha3 code
      isoNumber code
      Phone country code (ie: +1 (US))
      mobile_begin_with prefix codes
      Phone format lengths (ie: XXXYYYZZZZ (10))
      Postal code format & length
      Permitted non-postal characters
      Included postal validation regex
      Country States & State Codes (ie: "Alaska" : "AK" )
      
      //javascript:
      var obj = { dataset } ;
      console.log(obj.country["USA"]) ;

The above format uses lookup by the 3 character country code (IE: USA) and returns all info about that country.  But you can also do quick reverse lookups to get the the 3 character code if you only have country name or country 2 digit code:
  
    //Javascript
    var obj = { dataset } ;
    // extract country info with only 2 digit code
    console.log(obj.country[obj.alpha2_to_alpha3["US"]]) ;  
    // extract country info with only country name
    console.log(obj.country[obj.name_to_alpha3["United States"]] ;  

NOTE: Not all countries have postal info avaialble.  Either the information was incomplete or it simply does not exist for that country.  There are maybe a dozen that postal or so that don't have it.  Always test for `obj.country["XXX"].postal`

Sample Break Out of country-data object:

    {
        "country_formats": {
            "name_to_alpha3": {
                "United States": "USA",
                "Aruba": "ABW",
                "Afghanistan": "AFG",
            ...
            },
            "alpha2_to_alpha3": {
                "US": "USA",
                "AW": "ABW",
                "AF": "AFG",
             ...
             }
        },
        "country" : {
            "USA": {
                "info": {
                    "shortName": "United States",
                    "longName": "United States of America",
                    "alpha2": "US",
                    "alpha3": "USA",
                    "isoNumericCode": "840"
                },
                "phone": {
                    "countryCode": "1",
                    "mobile_begin_with": [
                        "201",
                        "202",
                        "203",
                        "205",
                        "206",
                        "207",
                        "208",
                        "209",
                        "210",
                        "212",
                        "213",
                        "214",
                        "215",
                        "216",
                        "217",
                        "218",
                        "219",
                        "224",
                        "225",
                        "227",
                        "228",
                        "229",
                        "231",
                        "234",
                        "239",
                        "240",
                        "248",
                        "251",
                        "252",
                        "253",
                        "254",
                        "256",
                        "260",
                        "262",
                        "267",
                        "269",
                        "270",
                        "272",
                        "274",
                        "276",
                        "278",
                        "281",
                        "283",
                        "301",
                        "302",
                        "303",
                        "304",
                        "305",
                        "307",
                        "308",
                        "309",
                        "310",
                        "312",
                        "313",
                        "314",
                        "315",
                        "316",
                        "317",
                        "318",
                        "319",
                        "320",
                        "321",
                        "323",
                        "325",
                        "327",
                        "330",
                        "331",
                        "334",
                        "336",
                        "337",
                        "339",
                        "341",
                        "346",
                        "347",
                        "351",
                        "352",
                        "360",
                        "361",
                        "364",
                        "369",
                        "380",
                        "385",
                        "386",
                        "401",
                        "402",
                        "404",
                        "405",
                        "406",
                        "407",
                        "408",
                        "409",
                        "410",
                        "412",
                        "413",
                        "414",
                        "415",
                        "417",
                        "419",
                        "423",
                        "424",
                        "425",
                        "430",
                        "432",
                        "434",
                        "435",
                        "440",
                        "442",
                        "443",
                        "445",
                        "447",
                        "458",
                        "464",
                        "469",
                        "470",
                        "475",
                        "478",
                        "479",
                        "480",
                        "484",
                        "501",
                        "502",
                        "503",
                        "504",
                        "505",
                        "507",
                        "508",
                        "509",
                        "510",
                        "512",
                        "513",
                        "515",
                        "516",
                        "517",
                        "518",
                        "520",
                        "530",
                        "531",
                        "534",
                        "539",
                        "540",
                        "541",
                        "551",
                        "557",
                        "559",
                        "561",
                        "562",
                        "563",
                        "564",
                        "567",
                        "570",
                        "571",
                        "573",
                        "574",
                        "575",
                        "580",
                        "582",
                        "585",
                        "586",
                        "601",
                        "602",
                        "603",
                        "605",
                        "606",
                        "607",
                        "608",
                        "609",
                        "610",
                        "612",
                        "614",
                        "615",
                        "616",
                        "617",
                        "618",
                        "619",
                        "620",
                        "623",
                        "626",
                        "627",
                        "628",
                        "629",
                        "630",
                        "631",
                        "636",
                        "641",
                        "646",
                        "650",
                        "651",
                        "657",
                        "659",
                        "660",
                        "661",
                        "662",
                        "667",
                        "669",
                        "678",
                        "679",
                        "681",
                        "682",
                        "689",
                        "701",
                        "702",
                        "703",
                        "704",
                        "706",
                        "707",
                        "708",
                        "712",
                        "713",
                        "714",
                        "715",
                        "716",
                        "717",
                        "718",
                        "719",
                        "720",
                        "724",
                        "725",
                        "727",
                        "730",
                        "731",
                        "732",
                        "734",
                        "737",
                        "740",
                        "747",
                        "752",
                        "754",
                        "757",
                        "760",
                        "762",
                        "763",
                        "764",
                        "765",
                        "769",
                        "770",
                        "772",
                        "773",
                        "774",
                        "775",
                        "779",
                        "781",
                        "785",
                        "786",
                        "801",
                        "802",
                        "803",
                        "804",
                        "805",
                        "806",
                        "808",
                        "810",
                        "812",
                        "813",
                        "814",
                        "815",
                        "816",
                        "817",
                        "818",
                        "828",
                        "830",
                        "831",
                        "832",
                        "835",
                        "843",
                        "845",
                        "847",
                        "848",
                        "850",
                        "854",
                        "856",
                        "857",
                        "858",
                        "859",
                        "860",
                        "862",
                        "863",
                        "864",
                        "865",
                        "870",
                        "872",
                        "878",
                        "901",
                        "903",
                        "904",
                        "906",
                        "907",
                        "908",
                        "909",
                        "910",
                        "912",
                        "913",
                        "914",
                        "915",
                        "916",
                        "917",
                        "918",
                        "919",
                        "920",
                        "925",
                        "927",
                        "928",
                        "929",
                        "931",
                        "934",
                        "935",
                        "936",
                        "937",
                        "938",
                        "940",
                        "941",
                        "947",
                        "949",
                        "951",
                        "952",
                        "954",
                        "956",
                        "957",
                        "959",
                        "970",
                        "971",
                        "972",
                        "973",
                        "975",
                        "978",
                        "979",
                        "980",
                        "984",
                        "985",
                        "986",
                        "989"
                    ],
                    "phone_number_lengths": [
                        10
                    ]
                },
                "postal": {
                    "Description": "US : NNNNN[-NNNN]",
                    "RedundantCharacters": " -",
                    "ValidationRegex": "^[0-9]{5}([0-9]{4})?$"
                },
                "states": {
                    "Alaska": "AK",
                    "Alabama": "AL",
                    "American Samoa": "AS",
                    "Arizona": "AZ",
                    "Arkansas": "AR",
                    "California": "CA",
                    "Colorado": "CO",
                    "Connecticut": "CT",
                    "Delaware": "DE",
                    "District of Columbia": "DC",
                    "Micronesia": "FM",
                    "Florida": "FL",
                    "Georgia": "GA",
                    "Guam": "GU",
                    "Hawaii": "HI",
                    "Idaho": "ID",
                    "Illinois": "IL",
                    "Indiana": "IN",
                    "Iowa": "IA",
                    "Kansas": "KS",
                    "Kentucky": "KY",
                    "Louisiana": "LA",
                    "Maine": "ME",
                    "Marshall Islands": "MH",
                    "Maryland": "MD",
                    "Massachusetts": "MA",
                    "Michigan": "MI",
                    "Minnesota": "MN",
                    "Mississippi": "MS",
                    "Missouri": "MO",
                    "Montana": "MT",
                    "Nebraska": "NE",
                    "Nevada": "NV",
                    "New Hampshire": "NH",
                    "New Jersey": "NJ",
                    "New Mexico": "NM",
                    "New York": "NY",
                    "North Carolina": "NC",
                    "North Dakota": "ND",
                    "Northern Mariana Islands": "MP",
                    "Ohio": "OH",
                    "Oklahoma": "OK",
                    "Oregon": "OR",
                    "Palau": "PW",
                    "Pennsylvania": "PA",
                    "Puerto Rico": "PR",
                    "Rhode Island": "RI",
                    "South Carolina": "SC",
                    "South Dakota": "SD",
                    "Tennessee": "TN",
                    "Texas": "TX",
                    "Utah": "UT",
                    "Vermont": "VT",
                    "Virgin Islands": "VI",
                    "Virginia": "VA",
                    "Washington": "WA",
                    "West Virginia": "WV",
                    "Wisconsin": "WI",
                    "Wyoming": "WY",
                    "Armed Forces Americas": "AA",
                    "Armed Forces Europe, Canada, Africa and Middle East": "AE",
                    "Armed Forces Pacific": "AP"
                }
            },
            "ABW": {
                "info": {
                    "shortName": "Aruba",
                    "longName": "Aruba",
                    "alpha2": "AW",
                    "alpha3": "ABW",
                    "isoNumericCode": "533"
                },
                "phone": {
                    "countryCode": "297",
                    "mobile_begin_with": [
                        "5",
                        "6",
                        "7",
                        "9"
                    ],
                    "phone_number_lengths": [
                        7
                    ]
                },
                "postal": {},
                "states": {
                    "Aruba": "AW"
                }
            },
            "AFG": {
                "info": {
                    "shortName": "Afghanistan",
                    "longName": "Afghanistan",
                    "alpha2": "AF",
                    "alpha3": "AFG",
                    "isoNumericCode": "4"
                },
                "phone": {
                    "countryCode": "93",
                    "mobile_begin_with": [
                        "7"
                    ],
                    "phone_number_lengths": [
                        9
                    ]
                },
                "postal": {
                    "Description": "4-Digits - NNNN",
                    "RedundantCharacters": " -",
                    "ValidationRegex": "^[0-9]{4}$"
                },
                "states": {
                    "Badakhshan": "BDS",
                    "Badghis": "BDG",
                    "Baghlan": "BGL",
                    "Balkh": "BAL",
                    "Bamyan": "BAM",
                    "Daykundi": "DAY",
                    "Farah": "FRA",
                    "Faryab": "FYB",
                    "Ghazni": "GHA",
                    "Ghor": "GHO",
                    "Helmand": "HEL",
                    "Herat": "HER",
                    "Jowzjan": "JOW",
                    "Kabul": "KAB",
                    "Kandahar": "KAN",
                    "Kapisa": "KAP",
                    "Khost": "KHO",
                    "Kunar": "KNR",
                    "Kunduz": "KDZ",
                    "Laghman": "LAG",
                    "Logar": "LOW",
                    "Maidan Wardak": "WAR",
                    "Nangarhar": "NAN",
                    "Nimruz": "NIM",
                    "Nuristan": "NUR",
                    "Paktia": "PIA",
                    "Paktika": "PKA",
                    "Panjshir": "PAN",
                    "Parwan": "PAR",
                    "Samangan": "SAM",
                    "Sar-e Pol": "SAR",
                    "Takhar": "TAK",
                    "Urozgan": "ORU",
                    "Zabul": "ZAB"
                }
            },
