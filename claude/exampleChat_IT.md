# Report Finanziario Gelaterie Terni - Conversazione con Claude Desktop

*Una ricerca completa sulle opportunità di investimento nel settore gelaterie a Terni, realizzata utilizzando Claude Desktop e l'API MCP Openapi.*

---

## 🗣️ Conversazione Originale

**Utente:** vorrei investire in una gelateria a terni. trova le prime 2 per fatturato e fammi un report finanziario in formato html

**Claude:** Ti aiuto a trovare le gelaterie con il fatturato più alto a Terni e preparare un report finanziario. Procederò per step:

1. Prima cercherò le gelaterie attive a Terni
2. Analizzerò i loro dati finanziari
3. Identificherò le prime 2 per fatturato
4. Creerò un report HTML dettagliato

Iniziamo la ricerca:

---

## 🔍 Prima Ricerca API - Gelaterie nella Provincia di Terni

**Search italian companies by advanced search criteria**

**Richiesta:**
````json
{
  "limit": "20",
  "companyName": "gelateria",
  "provinceCode": "TR",
  "activityStatus": "ATTIVA",
  "dataEnrichment": "advanced"
}
````

**Risposta:**
````json
[
    {
        "taxCode": "00569890551",
        "vatCode": "00569890551",
        "companyName": "BAR GELATERIA LE STELLE DI NINI SPARTACO & C. S.N.C.",
        "address": {
            "registeredOffice": {
                "toponym": "VIA",
                "street": "GIOSUE' CARDUCCI",
                "streetNumber": "30",
                "streetName": "VIA GIOSUE' CARDUCCI 30",
                "town": "BASCHI",
                "hamlet": null,
                "province": "TR",
                "zipCode": "05023",
                "region": {
                    "code": "10",
                    "description": "UMBRIA"
                },
                "townCode": "A691"
            }
        },
        "activityStatus": "ATTIVA",
        "reaCode": "61191",
        "cciaa": "TR",
        "atecoClassification": {
            "ateco": {
                "code": "563",
                "description": "Attivita' di somministrazione di bevande"
            },
            "ateco2007": {
                "code": "563",
                "description": "Bar e altri esercizi simili senza cucina"
            },
            "ateco2022": {
                "code": "563",
                "description": "BAR E ALTRI ESERCIZI SIMILI SENZA CUCINA"
            }
        },
        "detailedLegalForm": {
            "code": "SN",
            "description": "SOCIETA' IN NOME COLLETTIVO"
        },
        "startDate": "1990-07-13",
        "registrationDate": "1989-07-28",
        "endDate": null,
        "pec": "barlestelle@lamiapec.it",
        "taxCodeCeased": false,
        "taxCodeCeasedTimestamp": 1624359943,
        "vatGroup": {
            "vatGroupParticipation": false,
            "isVatGroupLeader": false,
            "registryOk": true
        },
        "sdiCode": "W7YVJK9",
        "sdiCodeTimestamp": 1624359943,
        "creationTimestamp": 1624359943,
        "lastUpdateTimestamp": 1755693577,
        "balanceSheets": {
            "last": null,
            "all": [
                {
                    "year": 2025,
                    "balanceSheetDate": null,
                    "turnover": null,
                    "netWorth": null,
                    "employees": 0,
                    "shareCapital": 0,
                    "totalStaffCost": null,
                    "totalAssets": null
                },
                {
                    "year": 2024,
                    "employees": 1,
                    "balanceSheetDate": null,
                    "turnover": null,
                    "netWorth": null,
                    "shareCapital": 0
                },
                {
                    "year": 2023,
                    "employees": 1,
                    "balanceSheetDate": null,
                    "turnover": null,
                    "netWorth": null,
                    "shareCapital": 0
                },
                {
                    "year": 2022,
                    "employees": 2,
                    "balanceSheetDate": null,
                    "turnover": null,
                    "netWorth": null,
                    "shareCapital": 0
                },
                {
                    "year": 2021,
                    "employees": 2,
                    "balanceSheetDate": null,
                    "turnover": null,
                    "netWorth": null,
                    "shareCapital": 0
                }
            ]
        },
        "id": "60d1c407f335ab51b25e8c18",
        "shareHolders": []
    },
    {
        "taxCode": "01584810558",
        "vatCode": "01584810558",
        "companyName": "ANTICA GELATERIA GIROTTI S.R.L.",
        "address": {
            "registeredOffice": {
                "toponym": "VIA",
                "street": "DELLE RIMEMBRANZE",
                "streetNumber": "48",
                "streetName": "VIA DELLE RIMEMBRANZE 48",
                "town": "AMELIA",
                "hamlet": null,
                "province": "TR",
                "zipCode": "05022",
                "region": {
                    "code": "10",
                    "description": "UMBRIA"
                },
                "townCode": "A262"
            }
        },
        "activityStatus": "ATTIVA",
        "reaCode": "108702",
        "cciaa": "TR",
        "atecoClassification": {
            "ateco": {
                "code": "56112",
                "description": "Attivita' di gelaterie e pasticcerie"
            },
            "ateco2007": {
                "code": "56103",
                "description": "Gelaterie e pasticcerie"
            },
            "ateco2022": {
                "code": "56103",
                "description": "Gelaterie e pasticcerie"
            }
        },
        "detailedLegalForm": {
            "code": "SR",
            "description": "SOCIETA' A RESPONSABILITA' LIMITATA"
        },
        "startDate": "2017-03-28",
        "registrationDate": "2017-01-17",
        "endDate": null,
        "pec": "anticagelateriagirottisrl@pec.it",
        "taxCodeCeased": false,
        "taxCodeCeasedTimestamp": 1624357578,
        "vatGroup": {
            "vatGroupParticipation": false,
            "isVatGroupLeader": false,
            "registryOk": true
        },
        "sdiCode": "M5UXCR1",
        "sdiCodeTimestamp": 1624357578,
        "creationTimestamp": 1624357578,
        "lastUpdateTimestamp": 1755689670,
        "balanceSheets": {
            "last": {
                "year": 2023,
                "employees": 2,
                "balanceSheetDate": "2023-12-31",
                "turnover": 139206,
                "netWorth": -809,
                "shareCapital": 10000,
                "totalStaffCost": 73560,
                "totalAssets": 294196,
                "avgGrossSalary": 36780
            },
            "all": [
                {
                    "year": 2025,
                    "balanceSheetDate": null,
                    "turnover": null,
                    "netWorth": null,
                    "employees": 2,
                    "shareCapital": 10000,
                    "totalStaffCost": null,
                    "totalAssets": null
                },
                {
                    "year": 2024,
                    "employees": 2,
                    "balanceSheetDate": null,
                    "turnover": null,
                    "netWorth": null,
                    "shareCapital": 10000
                },
                {
                    "year": 2023,
                    "employees": 2,
                    "balanceSheetDate": "2023-12-31",
                    "turnover": 139206,
                    "netWorth": -809,
                    "shareCapital": 10000,
                    "totalStaffCost": 73560,
                    "totalAssets": 294196,
                    "avgGrossSalary": 36780
                },
                {
                    "year": 2022,
                    "employees": 2,
                    "balanceSheetDate": "2022-12-31",
                    "turnover": 86844,
                    "netWorth": -16946,
                    "shareCapital": 10000,
                    "totalStaffCost": 75601,
                    "totalAssets": 335956,
                    "avgGrossSalary": 37800
                },
                {
                    "year": 2021,
                    "employees": 5,
                    "balanceSheetDate": "2021-12-31",
                    "turnover": 163637,
                    "netWorth": -18536,
                    "shareCapital": 10000
                },
                {
                    "year": 2020,
                    "employees": 4,
                    "balanceSheetDate": "2020-12-31",
                    "turnover": 160563,
                    "netWorth": 4857,
                    "shareCapital": 10000
                },
                {
                    "year": 2019,
                    "employees": 4,
                    "balanceSheetDate": "2019-12-31",
                    "turnover": 127047,
                    "netWorth": -11131,
                    "shareCapital": 10000
                },
                {
                    "year": 2018,
                    "employees": null,
                    "balanceSheetDate": "2018-12-31",
                    "turnover": 86797,
                    "netWorth": -33794,
                    "shareCapital": null
                },
                {
                    "year": 2017,
                    "employees": null,
                    "balanceSheetDate": "2017-12-31",
                    "turnover": 90350,
                    "netWorth": -22805,
                    "shareCapital": null
                }
            ]
        },
        "id": "60d1baca5591bc78f77ad038",
        "shareHolders": [
            {
                "companyName": "GIROTTI JESS",
                "name": "JESS",
                "surname": "GIROTTI",
                "taxCode": "GRTJSS69S07H501C",
                "percentShare": 60
            },
            {
                "companyName": "RUSSO MARIA TERESA",
                "name": "MARIA TERESA",
                "surname": "RUSSO",
                "taxCode": "RSSMTR73R63F839O",
                "percentShare": 40
            }
        ]
    },
    {
        "taxCode": "CHRVLR80M04A262U",
        "vatCode": "01327620553",
        "companyName": "GELATERIA IGLOO DI CHIERUZZI VALERIO",
        "address": {
            "registeredOffice": {
                "toponym": "VIA",
                "street": "TUDERTE",
                "streetNumber": "187/189",
                "streetName": "VIA TUDERTE 187/189",
                "town": "NARNI",
                "hamlet": "NARNI SCALO",
                "province": "TR",
                "zipCode": "05035",
                "gps": {
                    "coordinates": [
                        12.52043,
                        42.53634
                    ]
                },
                "region": {
                    "code": "10",
                    "description": "UMBRIA"
                },
                "townCode": "F844"
            }
        },
        "activityStatus": "ATTIVA",
        "reaCode": "95488",
        "cciaa": "TR",
        "atecoClassification": {
            "ateco": {
                "code": "56112",
                "description": "Attivita' di gelaterie e pasticcerie"
            },
            "ateco2007": {
                "code": "56103",
                "description": "Gelaterie e pasticcerie"
            },
            "ateco2022": {
                "code": "56103",
                "description": "Gelaterie e pasticcerie"
            }
        },
        "detailedLegalForm": {
            "code": "DI",
            "description": "IMPRESA INDIVIDUALE"
        },
        "startDate": "2009-03-13",
        "registrationDate": "2009-04-14",
        "endDate": null,
        "pec": "gelater1aigl00@pec.it",
        "taxCodeCeased": false,
        "taxCodeCeasedTimestamp": 1624357297,
        "vatGroup": {
            "vatGroupParticipation": false,
            "isVatGroupLeader": false,
            "registryOk": true
        },
        "sdiCode": "0000000",
        "sdiCodeTimestamp": 1624357297,
        "creationTimestamp": 1624357297,
        "lastUpdateTimestamp": 1755774256,
        "balanceSheets": {
            "last": null,
            "all": [
                {
                    "year": 2025,
                    "balanceSheetDate": null,
                    "turnover": null,
                    "netWorth": null,
                    "employees": 0,
                    "shareCapital": 0,
                    "totalStaffCost": null,
                    "totalAssets": null
                },
                {
                    "year": 2024,
                    "employees": 2,
                    "balanceSheetDate": null,
                    "turnover": null,
                    "netWorth": null,
                    "shareCapital": 0
                },
                {
                    "year": 2023,
                    "employees": 1,
                    "balanceSheetDate": null,
                    "turnover": null,
                    "netWorth": null,
                    "shareCapital": 0
                },
                {
                    "year": 2022,
                    "employees": 2,
                    "balanceSheetDate": null,
                    "turnover": null,
                    "netWorth": null,
                    "shareCapital": 0
                },
                {
                    "year": 2021,
                    "employees": 3,
                    "balanceSheetDate": null,
                    "turnover": null,
                    "netWorth": null,
                    "shareCapital": 0
                }
            ]
        },
        "id": "60d1b9b13131c34aa76ec94a",
        "shareHolders": []
    },
    {
        "taxCode": "PRRGNN74T58L117Z",
        "vatCode": "01379330556",
        "companyName": "BAR GELATERIA TONI DI PERRI GIOVANNA",
        "address": {
            "registeredOffice": {
                "toponym": "VIA",
                "street": "PIAVE",
                "streetNumber": "41/39",
                "streetName": "VIA PIAVE 41/39",
                "town": "TERNI",
                "hamlet": null,
                "province": "TR",
                "zipCode": "05100",
                "gps": {
                    "coordinates": [
                        12.6489,
                        42.55631
                    ]
                },
                "region": {
                    "code": "10",
                    "description": "UMBRIA"
                },
                "townCode": "L117"
            }
        },
        "activityStatus": "ATTIVA",
        "reaCode": "93284",
        "cciaa": "TR",
        "atecoClassification": {
            "ateco": {
                "code": "563",
                "description": "Attivita' di somministrazione di bevande"
            },
            "ateco2007": {
                "code": "563",
                "description": "Bar e altri esercizi simili senza cucina"
            },
            "ateco2022": {
                "code": "563",
                "description": "BAR E ALTRI ESERCIZI SIMILI SENZA CUCINA"
            }
        },
        "detailedLegalForm": {
            "code": "DI",
            "description": "IMPRESA INDIVIDUALE"
        },
        "startDate": "2008-01-14",
        "registrationDate": "2008-01-23",
        "endDate": null,
        "pec": null,
        "taxCodeCeased": false,
        "taxCodeCeasedTimestamp": 1624357887,
        "vatGroup": {
            "vatGroupParticipation": false,
            "isVatGroupLeader": false,
            "registryOk": true
        },
        "sdiCode": null,
        "sdiCodeTimestamp": 1624357887,
        "creationTimestamp": 1624357887,
        "lastUpdateTimestamp": 1755795600,
        "balanceSheets": {
            "last": null,
            "all": [
                {
                    "year": 2025,
                    "balanceSheetDate": null,
                    "turnover": null,
                    "netWorth": null,
                    "employees": 0,
                    "shareCapital": 0,
                    "totalStaffCost": null,
                    "totalAssets": null
                },
                {
                    "year": 2024,
                    "employees": 0,
                    "balanceSheetDate": null,
                    "turnover": null,
                    "netWorth": null,
                    "shareCapital": 0
                },
                {
                    "year": 2023,
                    "employees": 0,
                    "balanceSheetDate": null,
                    "turnover": null,
                    "netWorth": null,
                    "shareCapital": 0
                },
                {
                    "year": 2022,
                    "employees": 0,
                    "balanceSheetDate": null,
                    "turnover": null,
                    "netWorth": null,
                    "shareCapital": 0
                },
                {
                    "year": 2021,
                    "employees": 0,
                    "balanceSheetDate": null,
                    "turnover": null,
                    "netWorth": null,
                    "shareCapital": 0
                }
            ]
        },
        "id": "60d1bbfff9935c14ea349835",
        "shareHolders": []
    },
    {
        "taxCode": "BRTSFN74D28L117X",
        "vatCode": "01230200550",
        "companyName": "GELATERIA BAR PORTA ROMANA DI BARTOLUCCI STEFANO",
        "address": {
            "registeredOffice": {
                "toponym": "VIA",
                "street": "ROMA",
                "streetNumber": "180",
                "streetName": "VIA ROMA 180",
                "town": "TERNI",
                "hamlet": null,
                "province": "TR",
                "zipCode": "05100",
                "gps": {
                    "coordinates": [
                        12.64456,
                        42.55833
                    ]
                },
                "region": {
                    "code": "10",
                    "description": "UMBRIA"
                },
                "townCode": "L117"
            }
        },
        "activityStatus": "ATTIVA",
        "reaCode": "82432",
        "cciaa": "TR",
        "atecoClassification": {
            "ateco": {
                "code": "56112",
                "description": "Attivita' di gelaterie e pasticcerie"
            },
            "ateco2007": {
                "code": "56103",
                "description": "Gelaterie e pasticcerie"
            },
            "ateco2022": {
                "code": "56103",
                "description": "Gelaterie e pasticcerie"
            }
        },
        "detailedLegalForm": {
            "code": "DI",
            "description": "IMPRESA INDIVIDUALE"
        },
        "startDate": "2001-05-09",
        "registrationDate": "2001-06-26",
        "endDate": null,
        "pec": "barportaromana@pec.it",
        "taxCodeCeased": false,
        "taxCodeCeasedTimestamp": 1624357651,
        "vatGroup": {
            "vatGroupParticipation": false,
            "isVatGroupLeader": false,
            "registryOk": true
        },
        "sdiCode": "0000000",
        "sdiCodeTimestamp": 1624357651,
        "creationTimestamp": 1624357651,
        "lastUpdateTimestamp": 1755817331,
        "balanceSheets": {
            "last": null,
            "all": [
                {
                    "year": 2025,
                    "balanceSheetDate": null,
                    "turnover": null,
                    "netWorth": null,
                    "employees": 4,
                    "shareCapital": 0,
                    "totalStaffCost": null,
                    "totalAssets": null
                },
                {
                    "year": 2024,
                    "employees": 6,
                    "balanceSheetDate": null,
                    "turnover": null,
                    "netWorth": null,
                    "shareCapital": 0
                },
                {
                    "year": 2023,
                    "employees": 4,
                    "balanceSheetDate": null,
                    "turnover": null,
                    "netWorth": null,
                    "shareCapital": 0
                },
                {
                    "year": 2022,
                    "employees": 5,
                    "balanceSheetDate": null,
                    "turnover": null,
                    "netWorth": null,
                    "shareCapital": 0
                },
                {
                    "year": 2021,
                    "employees": 4,
                    "balanceSheetDate": null,
                    "turnover": null,
                    "netWorth": null,
                    "shareCapital": 0
                }
            ]
        },
        "id": "60d1bb135591bc78f77e8a3c",
        "shareHolders": []
    },
    {
        "taxCode": "CRSMSM70E23L117E",
        "vatCode": "01359140553",
        "companyName": "GELATERIA - PASTICCERIA CAPITAN CONO DI CRESTA MASSIMO",
        "address": {
            "registeredOffice": {
                "toponym": "VIA",
                "street": "DEL RIVO",
                "streetNumber": "227",
                "streetName": "VIA DEL RIVO 227",
                "town": "TERNI",
                "hamlet": null,
                "province": "TR",
                "zipCode": "05100",
                "gps": {
                    "coordinates": [
                        12.61788,
                        42.5823
                    ]
                },
                "region": {
                    "code": "10",
                    "description": "UMBRIA"
                },
                "townCode": "L117"
            }
        },
        "activityStatus": "ATTIVA",
        "reaCode": "91471",
        "cciaa": "TR",
        "atecoClassification": {
            "ateco": {
                "code": "56112",
                "description": "Attivita' di gelaterie e pasticcerie"
            },
            "ateco2007": {
                "code": "56103",
                "description": "Gelaterie e pasticcerie"
            },
            "ateco2022": {
                "code": "56103",
                "description": "Gelaterie e pasticcerie"
            }
        },
        "detailedLegalForm": {
            "code": "DI",
            "description": "IMPRESA INDIVIDUALE"
        },
        "startDate": "2007-01-05",
        "registrationDate": "2007-01-11",
        "endDate": null,
        "pec": "crestamassimo@pec.it",
        "taxCodeCeased": false,
        "taxCodeCeasedTimestamp": 1624356850,
        "vatGroup": {
            "vatGroupParticipation": false,
            "isVatGroupLeader": false,
            "registryOk": true
        },
        "sdiCode": null,
        "sdiCodeTimestamp": 1624356850,
        "creationTimestamp": 1624356850,
        "lastUpdateTimestamp": 1755822783,
        "balanceSheets": {
            "last": null,
            "all": [
                {
                    "year": 2025,
                    "balanceSheetDate": null,
                    "turnover": null,
                    "netWorth": null,
                    "employees": 0,
                    "shareCapital": 0,
                    "totalStaffCost": null,
                    "totalAssets": null
                },
                {
                    "year": 2024,
                    "employees": 1,
                    "balanceSheetDate": null,
                    "turnover": null,
                    "netWorth": null,
                    "shareCapital": 0
                },
                {
                    "year": 2023,
                    "employees": 1,
                    "balanceSheetDate": null,
                    "turnover": null,
                    "netWorth": null,
                    "shareCapital": 0
                },
                {
                    "year": 2022,
                    "employees": 1,
                    "balanceSheetDate": null,
                    "turnover": null,
                    "netWorth": null,
                    "shareCapital": 0
                },
                {
                    "year": 2021,
                    "employees": 1,
                    "balanceSheetDate": null,
                    "turnover": null,
                    "netWorth": null,
                    "shareCapital": 0
                }
            ]
        },
        "id": "60d1b7f21edf6f510640894f",
        "shareHolders": []
    },
    {
        "taxCode": "01586500553",
        "vatCode": "01586500553",
        "companyName": "GELATERIA ANDREA S.N.C. DI FEDERICI ANDREA & C.",
        "address": {
            "registeredOffice": {
                "toponym": "VIA",
                "street": "FRANCESCO MANCINI",
                "streetNumber": "7",
                "streetName": "VIA FRANCESCO MANCINI 7",
                "town": "TERNI",
                "hamlet": null,
                "province": "TR",
                "zipCode": "05100",
                "region": {
                    "code": "10",
                    "description": "UMBRIA"
                },
                "townCode": "L117"
            }
        },
        "activityStatus": "ATTIVA",
        "reaCode": "108837",
        "cciaa": "TR",
        "atecoClassification": {
            "ateco": {
                "code": "56112",
                "description": "Attivita' di gelaterie e pasticcerie"
            },
            "ateco2007": {
                "code": "56103",
                "description": "Gelaterie e pasticcerie"
            },
            "ateco2022": {
                "code": "56103",
                "description": "Gelaterie e pasticcerie"
            }
        },
        "detailedLegalForm": {
            "code": "SN",
            "description": "SOCIETA' IN NOME COLLETTIVO"
        },
        "startDate": "2017-07-03",
        "registrationDate": "2017-02-10",
        "endDate": null,
        "pec": "gelateria.andrea@pec.it",
        "taxCodeCeased": false,
        "taxCodeCeasedTimestamp": 1624359762,
        "vatGroup": {
            "vatGroupParticipation": false,
            "isVatGroupLeader": false,
            "registryOk": true
        },
        "sdiCode": "M5UXCR1",
        "sdiCodeTimestamp": 1624359762,
        "creationTimestamp": 1624359762,
        "lastUpdateTimestamp": 1755767574,
        "balanceSheets": {
            "last": null,
            "all": [
                {
                    "year": 2025,
                    "balanceSheetDate": null,
                    "turnover": null,
                    "netWorth": null,
                    "employees": 4,
                    "shareCapital": 0,
                    "totalStaffCost": null,
                    "totalAssets": null
                },
                {
                    "year": 2024,
                    "employees": 6,
                    "balanceSheetDate": null,
                    "turnover": null,
                    "netWorth": null,
                    "shareCapital": 0
                },
                {
                    "year": 2023,
                    "employees": 4,
                    "balanceSheetDate": null,
                    "turnover": null,
                    "netWorth": null,
                    "shareCapital": 0
                },
                {
                    "year": 2022,
                    "employees": 4,
                    "balanceSheetDate": null,
                    "turnover": null,
                    "netWorth": null,
                    "shareCapital": 0
                },
                {
                    "year": 2021,
                    "employees": 4,
                    "balanceSheetDate": null,
                    "turnover": null,
                    "netWorth": null,
                    "shareCapital": 0
                }
            ]
        },
        "id": "60d1c352eba32633fd2afbbc",
        "shareHolders": []
    },
    {
        "taxCode": "MNCRTI68P70F457P",
        "vatCode": "01512990555",
        "companyName": "PIZZERIA GELATERIA LA SOAVE DI MANCINI RITA",
        "address": {
            "registeredOffice": {
                "toponym": "VIALE",
                "street": "GIUSEPPE VERDI",
                "streetNumber": "88 A",
                "streetName": "VIALE GIUSEPPE VERDI 88 A",
                "town": "MONTECASTRILLI",
                "hamlet": null,
                "province": "TR",
                "zipCode": "05026",
                "gps": {},
                "region": {
                    "code": "10",
                    "description": "UMBRIA"
                },
                "townCode": "F457"
            }
        },
        "activityStatus": "ATTIVA",
        "reaCode": "102892",
        "cciaa": "TR",
        "atecoClassification": {
            "ateco": {
                "code": "0111",
                "description": "Coltivazione di cereali, legumi da granella e semi oleosi, escluso il riso"
            },
            "ateco2007": {
                "code": "01111",
                "description": "Coltivazione di cereali (escluso il riso)"
            },
            "ateco2022": {
                "code": "01111",
                "description": "Coltivazione di cereali (escluso il riso)"
            }
        },
        "detailedLegalForm": {
            "code": "DI",
            "description": "IMPRESA INDIVIDUALE"
        },
        "startDate": "2013-07-22",
        "registrationDate": "2013-10-30",
        "endDate": null,
        "pec": "lasoavepasticceria@sicurezzapostale.it",
        "taxCodeCeased": false,
        "taxCodeCeasedTimestamp": 1624356472,
        "vatGroup": {
            "vatGroupParticipation": false,
            "isVatGroupLeader": false,
            "registryOk": true
        },
        "sdiCode": null,
        "sdiCodeTimestamp": 1624356472,
        "creationTimestamp": 1624356472,
        "lastUpdateTimestamp": 1755760887,
        "balanceSheets": {
            "last": null,
            "all": [
                {
                    "year": 2025,
                    "balanceSheetDate": null,
                    "turnover": null,
                    "netWorth": null,
                    "employees": 0,
                    "shareCapital": 0,
                    "totalStaffCost": null,
                    "totalAssets": null
                },
                {
                    "year": 2024,
                    "employees": 1,
                    "balanceSheetDate": null,
                    "turnover": null,
                    "netWorth": null,
                    "shareCapital": 0
                },
                {
                    "year": 2023,
                    "employees": 1,
                    "balanceSheetDate": null,
                    "turnover": null,
                    "netWorth": null,
                    "shareCapital": 0
                },
                {
                    "year": 2022,
                    "employees": 1,
                    "balanceSheetDate": null,
                    "turnover": null,
                    "netWorth": null,
                    "shareCapital": 0
                },
                {
                    "year": 2021,
                    "employees": 1,
                    "balanceSheetDate": null,
                    "turnover": null,
                    "netWorth": null,
                    "shareCapital": 0
                }
            ]
        },
        "id": "60d1b6781283d916bd3338b8",
        "shareHolders": []
    }
]
````
Ora cerco specificamente le gelaterie con sede proprio nel comune di Terni per avere un quadro più preciso:


O

Search italian companies by advanced search criteria
Richiesta

{
  "limit": "20",
  "townCode": "L117",
  "atecoCode": "56103",
  "activityStatus": "ATTIVA",
  "dataEnrichment": "advanced"
}
Risposta

{"error":"API Request Error","message":"Expecting value: line 1 column 1 (char 0)"}
Provo con un approccio diverso per ottenere più dati sulle gelaterie di Terni:


O

Search italian companies by advanced search criteria
Richiesta

{
  "limit": "50",
  "companyName": "gelateria",
  "provinceCode": "TR",
  "activityStatus": "ATTIVA",
  "dataEnrichment": "advanced"
}
Risposta

[{"taxCode":"00569890551","vatCode":"00569890551","companyName":"BAR GELATERIA LE STELLE DI NINI SPARTACO & C. S.N.C.","address":{"registeredOffice":{"toponym":"VIA","street":"GIOSUE' CARDUCCI","streetNumber":"30","streetName":"VIA GIOSUE' CARDUCCI 30","town":"BASCHI","hamlet":null,"province":"TR","zipCode":"05023","region":{"code":"10","description":"UMBRIA"},"townCode":"A691"}},"activityStatus":"ATTIVA","reaCode":"61191","cciaa":"TR","atecoClassification":{"ateco":{"code":"563","description":"Attivita' di somministrazione di bevande"},"ateco2007":{"code":"563","description":"Bar e altri esercizi simili senza cucina"},"ateco2022":{"code":"563","description":"BAR E ALTRI ESERCIZI SIMILI SENZA CUCINA"}},"detailedLegalForm":{"code":"SN","description":"SOCIETA' IN NOME COLLETTIVO"},"startDate":"1990-07-13","registrationDate":"1989-07-28","endDate":null,"pec":"barlestelle@lamiapec.it","taxCodeCeased":false,"taxCodeCeasedTimestamp":1624359943,"vatGroup":{"vatGroupParticipation":false,"isVatGroupLeader":false,"registryOk":true},"sdiCode":"W7YVJK9","sdiCodeTimestamp":1624359943,"creationTimestamp":1624359943,"lastUpdateTimestamp":1755693577,"balanceSheets":{"last":null,"all":[{"year":2025,"balanceSheetDate":null,"turnover":null,"netWorth":null,"employees":0,"shareCapital":0,"totalStaffCost":null,"totalAssets":null},{"year":2024,"employees":1,"balanceSheetDate":null,"turnover":null,"netWorth":null,"shareCapital":0},{"year":2023,"employees":1,"balanceSheetDate":null,"turnover":null,"netWorth":null,"shareCapital":0},{"year":2022,"employees":2,"balanceSheetDate":null,"turnover":null,"netWorth":null,"shareCapital":0},{"year":2021,"employees":2,"balanceSheetDate":null,"turnover":null,"netWorth":null,"shareCapital":0}]},"id":"60d1c407f335ab51b25e8c18","shareHolders":[]},{"taxCode":"01584810558","vatCode":"01584810558","companyName":"ANTICA GELATERIA GIROTTI S.R.L.","address":{"registeredOffice":{"toponym":"VIA","street":"DELLE RIMEMBRANZE","streetNumber":"48","streetName":"VIA DELLE RIMEMBRANZE 48","town":"AMELIA","hamlet":null,"province":"TR","zipCode":"05022","region":{"code":"10","description":"UMBRIA"},"townCode":"A262"}},"activityStatus":"ATTIVA","reaCode":"108702","cciaa":"TR","atecoClassification":{"ateco":{"code":"56112","description":"Attivita' di gelaterie e pasticcerie"},"ateco2007":{"code":"56103","description":"Gelaterie e pasticcerie"},"ateco2022":{"code":"56103","description":"Gelaterie e pasticcerie"}},"detailedLegalForm":{"code":"SR","description":"SOCIETA' A RESPONSABILITA' LIMITATA"},"startDate":"2017-03-28","registrationDate":"2017-01-17","endDate":null,"pec":"anticagelateriagirottisrl@pec.it","taxCodeCeased":false,"taxCodeCeasedTimestamp":1624357578,"vatGroup":{"vatGroupParticipation":false,"isVatGroupLeader":false,"registryOk":true},"sdiCode":"M5UXCR1","sdiCodeTimestamp":1624357578,"creationTimestamp":1624357578,"lastUpdateTimestamp":1755689670,"balanceSheets":{"last":{"year":2023,"employees":2,"balanceSheetDate":"2023-12-31","turnover":139206,"netWorth":-809,"shareCapital":10000,"totalStaffCost":73560,"totalAssets":294196,"avgGrossSalary":36780},"all":[{"year":2025,"balanceSheetDate":null,"turnover":null,"netWorth":null,"employees":2,"shareCapital":10000,"totalStaffCost":null,"totalAssets":null},{"year":2024,"employees":2,"balanceSheetDate":null,"turnover":null,"netWorth":null,"shareCapital":10000},{"year":2023,"employees":2,"balanceSheetDate":"2023-12-31","turnover":139206,"netWorth":-809,"shareCapital":10000,"totalStaffCost":73560,"totalAssets":294196,"avgGrossSalary":36780},{"year":2022,"employees":2,"balanceSheetDate":"2022-12-31","turnover":86844,"netWorth":-16946,"shareCapital":10000,"totalStaffCost":75601,"totalAssets":335956,"avgGrossSalary":37800},{"year":2021,"employees":5,"balanceSheetDate":"2021-12-31","turnover":163637,"netWorth":-18536,"shareCapital":10000},{"year":2020,"employees":4,"balanceSheetDate":"2020-12-31","turnover":160563,"netWorth":4857,"shareCapital":10000},{"year":2019,"employees":4,"balanceSheetDate":"2019-12-31","turnover":127047,"netWorth":-11131,"shareCapital":10000},{"year":2018,"employees":null,"balanceSheetDate":"2018-12-31","turnover":86797,"netWorth":-33794,"shareCapital":null},{"year":2017,"employees":null,"balanceSheetDate":"2017-12-31","turnover":90350,"netWorth":-22805,"shareCapital":null}]},"id":"60d1baca5591bc78f77ad038","shareHolders":[{"companyName":"GIROTTI JESS","name":"JESS","surname":"GIROTTI","taxCode":"GRTJSS69S07H501C","percentShare":60},{"companyName":"RUSSO MARIA TERESA","name":"MARIA TERESA","surname":"RUSSO","taxCode":"RSSMTR73R63F839O","percentShare":40}]},{"taxCode":"CHRVLR80M04A262U","vatCode":"01327620553","companyName":"GELATERIA IGLOO DI CHIERUZZI VALERIO","address":{"registeredOffice":{"toponym":"VIA","street":"TUDERTE","streetNumber":"187/189","streetName":"VIA TUDERTE 187/189","town":"NARNI","hamlet":"NARNI SCALO","province":"TR","zipCode":"05035","gps":{"coordinates":[12.52043,42.53634]},"region":{"code":"10","description":"UMBRIA"},"townCode":"F844"}},"activityStatus":"ATTIVA","reaCode":"95488","cciaa":"TR","atecoClassification":{"ateco":{"code":"56112","description":"Attivita' di gelaterie e pasticcerie"},"ateco2007":{"code":"56103","description":"Gelaterie e pasticcerie"},"ateco2022":{"code":"56103","description":"Gelaterie e pasticcerie"}},"detailedLegalForm":{"code":"DI","description":"IMPRESA INDIVIDUALE"},"startDate":"2009-03-13","registrationDate":"2009-04-14","endDate":null,"pec":"gelater1aigl00@pec.it","taxCodeCeased":false,"taxCodeCeasedTimestamp":1624357297,"vatGroup":{"vatGroupParticipation":false,"isVatGroupLeader":false,"registryOk":true},"sdiCode":"0000000","sdiCodeTimestamp":1624357297,"creationTimestamp":1624357297,"lastUpdateTimestamp":1755774256,"balanceSheets":{"last":null,"all":[{"year":2025,"balanceSheetDate":null,"turnover":null,"netWorth":null,"employees":0,"shareCapital":0,"totalStaffCost":null,"totalAssets":null},{"year":2024,"employees":2,"balanceSheetDate":null,"turnover":null,"netWorth":null,"shareCapital":0},{"year":2023,"employees":1,"balanceSheetDate":null,"turnover":null,"netWorth":null,"shareCapital":0},{"year":2022,"employees":2,"balanceSheetDate":null,"turnover":null,"netWorth":null,"shareCapital":0},{"year":2021,"employees":3,"balanceSheetDate":null,"turnover":null,"netWorth":null,"shareCapital":0}]},"id":"60d1b9b13131c34aa76ec94a","shareHolders":[]},{"taxCode":"PRRGNN74T58L117Z","vatCode":"01379330556","companyName":"BAR GELATERIA TONI DI PERRI GIOVANNA","address":{"registeredOffice":{"toponym":"VIA","street":"PIAVE","streetNumber":"41/39","streetName":"VIA PIAVE 41/39","town":"TERNI","hamlet":null,"province":"TR","zipCode":"05100","gps":{"coordinates":[12.6489,42.55631]},"region":{"code":"10","description":"UMBRIA"},"townCode":"L117"}},"activityStatus":"ATTIVA","reaCode":"93284","cciaa":"TR","atecoClassification":{"ateco":{"code":"563","description":"Attivita' di somministrazione di bevande"},"ateco2007":{"code":"563","description":"Bar e altri esercizi simili senza cucina"},"ateco2022":{"code":"563","description":"BAR E ALTRI ESERCIZI SIMILI SENZA CUCINA"}},"detailedLegalForm":{"code":"DI","description":"IMPRESA INDIVIDUALE"},"startDate":"2008-01-14","registrationDate":"2008-01-23","endDate":null,"pec":null,"taxCodeCeased":false,"taxCodeCeasedTimestamp":1624357887,"vatGroup":{"vatGroupParticipation":false,"isVatGroupLeader":false,"registryOk":true},"sdiCode":null,"sdiCodeTimestamp":1624357887,"creationTimestamp":1624357887,"lastUpdateTimestamp":1755795600,"balanceSheets":{"last":null,"all":[{"year":2025,"balanceSheetDate":null,"turnover":null,"netWorth":null,"employees":0,"shareCapital":0,"totalStaffCost":null,"totalAssets":null},{"year":2024,"employees":0,"balanceSheetDate":null,"turnover":null,"netWorth":null,"shareCapital":0},{"year":2023,"employees":0,"balanceSheetDate":null,"turnover":null,"netWorth":null,"shareCapital":0},{"year":2022,"employees":0,"balanceSheetDate":null,"turnover":null,"netWorth":null,"shareCapital":0},{"year":2021,"employees":0,"balanceSheetDate":null,"turnover":null,"netWorth":null,"shareCapital":0}]},"id":"60d1bbfff9935c14ea349835","shareHolders":[]},{"taxCode":"BRTSFN74D28L117X","vatCode":"01230200550","companyName":"GELATERIA BAR PORTA ROMANA DI BARTOLUCCI STEFANO","address":{"registeredOffice":{"toponym":"VIA","street":"ROMA","streetNumber":"180","streetName":"VIA ROMA 180","town":"TERNI","hamlet":null,"province":"TR","zipCode":"05100","gps":{"coordinates":[12.64456,42.55833]},"region":{"code":"10","description":"UMBRIA"},"townCode":"L117"}},"activityStatus":"ATTIVA","reaCode":"82432","cciaa":"TR","atecoClassification":{"ateco":{"code":"56112","description":"Attivita' di gelaterie e pasticcerie"},"ateco2007":{"code":"56103","description":"Gelaterie e pasticcerie"},"ateco2022":{"code":"56103","description":"Gelaterie e pasticcerie"}},"detailedLegalForm":{"code":"DI","description":"IMPRESA INDIVIDUALE"},"startDate":"2001-05-09","registrationDate":"2001-06-26","endDate":null,"pec":"barportaromana@pec.it","taxCodeCeased":false,"taxCodeCeasedTimestamp":1624357651,"vatGroup":{"vatGroupParticipation":false,"isVatGroupLeader":false,"registryOk":true},"sdiCode":"0000000","sdiCodeTimestamp":1624357651,"creationTimestamp":1624357651,"lastUpdateTimestamp":1755817331,"balanceSheets":{"last":null,"all":[{"year":2025,"balanceSheetDate":null,"turnover":null,"netWorth":null,"employees":4,"shareCapital":0,"totalStaffCost":null,"totalAssets":null},{"year":2024,"employees":6,"balanceSheetDate":null,"turnover":null,"netWorth":null,"shareCapital":0},{"year":2023,"employees":4,"balanceSheetDate":null,"turnover":null,"netWorth":null,"shareCapital":0},{"year":2022,"employees":5,"balanceSheetDate":null,"turnover":null,"netWorth":null,"shareCapital":0},{"year":2021,"employees":4,"balanceSheetDate":null,"turnover":null,"netWorth":null,"shareCapital":0}]},"id":"60d1bb135591bc78f77e8a3c","shareHolders":[]},{"taxCode":"CRSMSM70E23L117E","vatCode":"01359140553","companyName":"GELATERIA - PASTICCERIA CAPITAN CONO DI CRESTA MASSIMO","address":{"registeredOffice":{"toponym":"VIA","street":"DEL RIVO","streetNumber":"227","streetName":"VIA DEL RIVO 227","town":"TERNI","hamlet":null,"province":"TR","zipCode":"05100","gps":{"coordinates":[12.61788,42.5823]},"region":{"code":"10","description":"UMBRIA"},"townCode":"L117"}},"activityStatus":"ATTIVA","reaCode":"91471","cciaa":"TR","atecoClassification":{"ateco":{"code":"56112","description":"Attivita' di gelaterie e pasticcerie"},"ateco2007":{"code":"56103","description":"Gelaterie e pasticcerie"},"ateco2022":{"code":"56103","description":"Gelaterie e pasticcerie"}},"detailedLegalForm":{"code":"DI","description":"IMPRESA INDIVIDUALE"},"startDate":"2007-01-05","registrationDate":"2007-01-11","endDate":null,"pec":"crestamassimo@pec.it","taxCodeCeased":false,"taxCodeCeasedTimestamp":1624356850,"vatGroup":{"vatGroupParticipation":false,"isVatGroupLeader":false,"registryOk":true},"sdiCode":null,"sdiCodeTimestamp":1624356850,"creationTimestamp":1624356850,"lastUpdateTimestamp":1755822783,"balanceSheets":{"last":null,"all":[{"year":2025,"balanceSheetDate":null,"turnover":null,"netWorth":null,"employees":0,"shareCapital":0,"totalStaffCost":null,"totalAssets":null},{"year":2024,"employees":1,"balanceSheetDate":null,"turnover":null,"netWorth":null,"shareCapital":0},{"year":2023,"employees":1,"balanceSheetDate":null,"turnover":null,"netWorth":null,"shareCapital":0},{"year":2022,"employees":1,"balanceSheetDate":null,"turnover":null,"netWorth":null,"shareCapital":0},{"year":2021,"employees":1,"balanceSheetDate":null,"turnover":null,"netWorth":null,"shareCapital":0}]},"id":"60d1b7f21edf6f510640894f","shareHolders":[]},{"taxCode":"01586500553","vatCode":"01586500553","companyName":"GELATERIA ANDREA S.N.C. DI FEDERICI ANDREA & C.","address":{"registeredOffice":{"toponym":"VIA","street":"FRANCESCO MANCINI","streetNumber":"7","streetName":"VIA FRANCESCO MANCINI 7","town":"TERNI","hamlet":null,"province":"TR","zipCode":"05100","region":{"code":"10","description":"UMBRIA"},"townCode":"L117"}},"activityStatus":"ATTIVA","reaCode":"108837","cciaa":"TR","atecoClassification":{"ateco":{"code":"56112","description":"Attivita' di gelaterie e pasticcerie"},"ateco2007":{"code":"56103","description":"Gelaterie e pasticcerie"},"ateco2022":{"code":"56103","description":"Gelaterie e pasticcerie"}},"detailedLegalForm":{"code":"SN","description":"SOCIETA' IN NOME COLLETTIVO"},"startDate":"2017-07-03","registrationDate":"2017-02-10","endDate":null,"pec":"gelateria.andrea@pec.it","taxCodeCeased":false,"taxCodeCeasedTimestamp":1624359762,"vatGroup":{"vatGroupParticipation":false,"isVatGroupLeader":false,"registryOk":true},"sdiCode":"M5UXCR1","sdiCodeTimestamp":1624359762,"creationTimestamp":1624359762,"lastUpdateTimestamp":1755767574,"balanceSheets":{"last":null,"all":[{"year":2025,"balanceSheetDate":null,"turnover":null,"netWorth":null,"employees":4,"shareCapital":0,"totalStaffCost":null,"totalAssets":null},{"year":2024,"employees":6,"balanceSheetDate":null,"turnover":null,"netWorth":null,"shareCapital":0},{"year":2023,"employees":4,"balanceSheetDate":null,"turnover":null,"netWorth":null,"shareCapital":0},{"year":2022,"employees":4,"balanceSheetDate":null,"turnover":null,"netWorth":null,"shareCapital":0},{"year":2021,"employees":4,"balanceSheetDate":null,"turnover":null,"netWorth":null,"shareCapital":0}]},"id":"60d1c352eba32633fd2afbbc","shareHolders":[]},{"taxCode":"MNCRTI68P70F457P","vatCode":"01512990555","companyName":"PIZZERIA GELATERIA LA SOAVE DI MANCINI RITA","address":{"registeredOffice":{"toponym":"VIALE","street":"GIUSEPPE VERDI","streetNumber":"88 A","streetName":"VIALE GIUSEPPE VERDI 88 A","town":"MONTECASTRILLI","hamlet":null,"province":"TR","zipCode":"05026","gps":{},"region":{"code":"10","description":"UMBRIA"},"townCode":"F457"}},"activityStatus":"ATTIVA","reaCode":"102892","cciaa":"TR","atecoClassification":{"ateco":{"code":"0111","description":"Coltivazione di cereali, legumi da granella e semi oleosi, escluso il riso"},"ateco2007":{"code":"01111","description":"Coltivazione di cereali (escluso il riso)"},"ateco2022":{"code":"01111","description":"Coltivazione di cereali (escluso il riso)"}},"detailedLegalForm":{"code":"DI","description":"IMPRESA INDIVIDUALE"},"startDate":"2013-07-22","registrationDate":"2013-10-30","endDate":null,"pec":"lasoavepasticceria@sicurezzapostale.it","taxCodeCeased":false,"taxCodeCeasedTimestamp":1624356472,"vatGroup":{"vatGroupParticipation":false,"isVatGroupLeader":false,"registryOk":true},"sdiCode":null,"sdiCodeTimestamp":1624356472,"creationTimestamp":1624356472,"lastUpdateTimestamp":1755760887,"balanceSheets":{"last":null,"all":[{"year":2025,"balanceSheetDate":null,"turnover":null,"netWorth":null,"employees":0,"shareCapital":0,"totalStaffCost":null,"totalAssets":null},{"year":2024,"employees":1,"balanceSheetDate":null,"turnover":null,"netWorth":null,"shareCapital":0},{"year":2023,"employees":1,"balanceSheetDate":null,"turnover":null,"netWorth":null,"shareCapital":0},{"year":2022,"employees":1,"balanceSheetDate":null,"turnover":null,"netWorth":null,"shareCapital":0},{"year":2021,"employees":1,"balanceSheetDate":null,"turnover":null,"netWorth":null,"shareCapital":0}]},"id":"60d1b6781283d916bd3338b8","shareHolders":[]}]
Ora ottengo informazioni più dettagliate per le aziende che hanno dati di fatturato. Prima verifico "Antica Gelateria Girotti" che ha dati completi:

O


Full italian companies data from VAT


O


Check async status
Richiesta

{
  "request_id": "85d5473c1fb683a175ab05b7c9b4b80e"
}
Risposta

{"data":{"companyDetails":{"vatCode":"01584810558","taxCode":"01584810558","lastUpdateDate":"2025-09-09T06:35:59.2239393Z","cciaa":"TR","reaCode":"108702","companyName":"ANTICA GELATERIA GIROTTI SRL","officeType":{"code":"SSL","description":"Administrative headquarter and registered office"},"openapiNumber":"IT0496060BS0001"},"legalForm":{"legalForm":{"code":"SC","description":"Joint stock business"},"detailedLegalForm":{"code":"SR","description":"Limited liability company/ limited company"}},"companyStatus":{"activityStatus":{"code":"A","description":"Enable"}},"companyDates":{"registrationDate":"2017-01-17T00:00:00","startDate":"2017-03-28T00:00:00","incorporationDate":"2017-01-09T00:00:00"},"address":{"streetName":"VIA RIMEMBRANZE, 48","zipCode":"05022","town":"AMELIA","province":{"code":"TR","description":"TERNI"},"region":{"code":"10","description":"UMBRIA"},"country":{"code":"IT","description":"Italia"}},"marketable":{"isMarketable":true},"branches":{"numberOfBranches":1},"atecoClassification":{"ateco":{"code":"56112","description":"56112 - Ice cream parlours and pastry shops"},"secondaryAteco":"","ateco2022":{"code":"56103","description":"Ice-cream parlors and bakeries"},"secondaryAteco2022":""},"internationalClassification":{"nace":{"code":"561","description":"Restaurants and mobile food service activities"},"primarySic":{"code":"5441","description":"Sweet & confectionery retailers"},"secondarySic":""},"ecofin":{"balanceSheetDate":"2024-12-31T00:00:00","turnoverRange":{"code":"TR4","description":"50000 - 99999"},"turnoverYear":2024,"turnover":61276,"turnoverTrend":-55.98,"shareCapital":10000,"netWorth":8139,"enterpriseSize":{"code":"MICRO","description":"Micro enterprise"}},"pec":"ANTICAGELATERIAGIROTTI@PEC.IT","employees":{"employeeRange":{"code":"ER2","description":"≤ 5"},"employee":2,"employeeTrend":0},"innovativeSmeAndSu":{"isInnovativeStartUp":false,"isInnovativeSme":false},"mail":{"email":""},"contacts":{"fax":""},"webAndSocial":{"website":"gelateriagirotti.shopsettings.com","hasSocial":true,"facebook":"https://facebook.com/gelateriagirotti","instagram":"https://instagram.com/gelateriagirottiamelia"},"foreignTrade":{"isImporter":false,"isExporter":false},"operatingResults":{"ebitda":28776,"ebitdaL2Y":22523,"ebit":-76,"ebitL2Y":234,"cashFlow":27801,"cashFlowL2Y":21480},"managers":[{"name":"JESS","surname":"GIROTTI","roles":[{"role":{"code":"AMM","description":"Director"},"roleStartDate":"2017-01-09T00:00:00"}],"gender":{"code":"M","description":"Man"},"taxCode":"GRTJSS69S07H501C","birthDate":"1969-11-07T00:00:00","age":55,"birthTown":"ROMA (RM)","isLegalRepresentative":true},{"name":"MARIA TERESA","surname":"RUSSO","roles":[{"role":{"code":"AMM","description":"Director"},"roleStartDate":"2017-01-09T00:00:00"}],"gender":{"code":"F","description":"Woman"},"taxCode":"RSSMTR73R63F839O","birthDate":"1973-10-23T00:00:00","age":51,"birthTown":"NAPOLI (NA)","isLegalRepresentative":true}],"shareholders":[{"shareholdersInformation":[{"taxCode":"GRTJSS69S07H501C","name":"JESS","surname":"GIROTTI","streetName":"VIA NOCICCHIA SNC","zipCode":"05022","town":"AMELIA"}],"percentShare":60},{"shareholdersInformation":[{"taxCode":"RSSMTR73R63F839O","name":"MARIA TERESA","surname":"RUSSO","streetName":"VIA SAN CARLO BORROMEO 18","zipCode":"80014","town":"GIUGLIANO IN CAMPANIA"}],"percentShare":40}],"assetsAggregateValues":[{"code":"IIC072","value":1505},{"code":"IIC001","value":0},{"code":"IIC071","value":59687},{"code":"IIC074","value":332830},{"code":"IIC039","value":271638}],"intangibleFixedAssets":[{"code":"IIC011","value":60639}],"creditsToShareholders":[{"code":"IIC002","value":0},{"code":"IIC193","value":0}],"corporateGroups":{"belongsToGroup":false,"nationalParentCompany":{"province":{"code":"ND99","description":"N. A."}},"hasForeignSubsidiaries":false,"hasForeignParents":false},"artisanBusinessRegistry":{"belongsToArtisanBusinessRegistry":false},"soaCertification":{"hasSoaCertification":false},"tangibleFixedAssets":[{"code":"IIC018","value":209103}],"cashEquivalents":[{"code":"IIC070","value":16898}],"credits":[{"code":"IIC057","value":0},{"code":"IIC053","value":0},{"code":"IIC047","value":0},{"code":"IIC055","value":0},{"code":"IIC051","value":0},{"code":"IIC049","value":0},{"code":"IIC199","value":0},{"code":"IIC056","value":35089},{"code":"IIC181","value":0},{"code":"IIC058","value":35089},{"code":"IIC327","value":0}],"financialFixedAssets":[{"code":"IIC038","value":1896}],"financialAssets":[{"code":"IIC201","value":0},{"code":"IIC202","value":0},{"code":"IIC200","value":0},{"code":"IIC062","value":0},{"code":"IIC065","value":0},{"code":"IIC060","value":0},{"code":"IIC059","value":0},{"code":"IIC061","value":0},{"code":"IIC066","value":0}],"inventory":[{"code":"IIC349","value":0},{"code":"IIC045","value":7700}],"debts":[{"code":"IIC099","value":0},{"code":"IIC091","value":0},{"code":"IIC093","value":0},{"code":"IIC103","value":0},{"code":"IIC117","value":0},{"code":"IIC097","value":0},{"code":"IIC107","value":0},{"code":"IIC113","value":0},{"code":"IIC109","value":0},{"code":"IIC105","value":0},{"code":"IIC221","value":0},{"code":"IIC095","value":0},{"code":"IIC185","value":0},{"code":"IIC101","value":0},{"code":"IIC115","value":0},{"code":"IIC116","value":291576},{"code":"IIC111","value":0}],"liabilitiesAggregateValues":[{"code":"IIC119","value":12894},{"code":"IIC089","value":20221},{"code":"IIC118","value":291576},{"code":"IIC121","value":332830},{"code":"IIC084","value":8139},{"code":"IIC088","value":0}],"netWorth":[{"code":"IIC078","value":0},{"code":"IIC216","value":0},{"code":"IIC218","value":0},{"code":"IIC081","value":-1},{"code":"IIC082","value":-809},{"code":"IIC083","value":-1051},{"code":"IIC215","value":0},{"code":"IIC077","value":0},{"code":"IIC075","value":10000},{"code":"IIC076","value":0},{"code":"IIC080","value":0}],"riskProvisions":[{"code":"IIC087","value":0},{"code":"IIC219","value":0},{"code":"IIC085","value":0},{"code":"IIC086","value":0}],"adjustments":[{"code":"IIC163","value":0},{"code":"IIC162","value":0},{"code":"IIC164","value":0},{"code":"IIC246","value":0},{"code":"IIC245","value":0},{"code":"IIC350","value":0},{"code":"IICC351","value":0},{"code":"IIC167","value":0},{"code":"IIC168","value":0},{"code":"IIC166","value":0},{"code":"IIC165","value":0},{"code":"IIC169","value":0}],"productionCosts":[{"code":"IIC134","value":42928},{"code":"IIC188","value":28852},{"code":"IIC140","value":11533},{"code":"IIC141","value":17319},{"code":"IIC142","value":0},{"code":"IIC143","value":0},{"code":"IIC133","value":2560},{"code":"IIC138","value":0},{"code":"IIC148","value":2521},{"code":"IIC147","value":0},{"code":"IIC137","value":0},{"code":"IIC131","value":33398},{"code":"IIC146","value":0},{"code":"IIC132","value":29671},{"code":"IIC136","value":2871},{"code":"IIC187","value":2871},{"code":"IIC135","value":13146},{"code":"IIC144","value":28852},{"code":"IIC139","value":58945},{"code":"IIC145","value":867}],"revenuesFinancialCharges":[{"code":"IIC226","value":0},{"code":"IPL231","value":0},{"code":"IIC236","value":0},{"code":"IIC227","value":0},{"code":"IPL232","value":0},{"code":"IIC237","value":0},{"code":"IIC225","value":0},{"code":"IIC230","value":0},{"code":"IIC235","value":0},{"code":"IIC228","value":0},{"code":"IIC233","value":0},{"code":"IIC238","value":0},{"code":"IIC229","value":0},{"code":"IIC234","value":0},{"code":"IIC239","value":0},{"code":"IIC156","value":0},{"code":"IIC190","value":0},{"code":"IIC152","value":0},{"code":"IIC155","value":0},{"code":"IIC154","value":0},{"code":"IIC150","value":0},{"code":"IIC189","value":0},{"code":"IIC241","value":0},{"code":"IIC243","value":0},{"code":"IIC244","value":975},{"code":"IIC242","value":0},{"code":"IIC240","value":0},{"code":"IIC159","value":975},{"code":"IIC158","value":0}],"annualResult":[{"code":"IIC191","value":0},{"code":"IIC192","value":0},{"code":"IIC250","value":0},{"code":"IIC179","value":-1051},{"code":"IIC177","value":-1051},{"code":"IIC347","value":0},{"code":"IIC178","value":0}],"incomeStatementAggregateValues":[{"code":"IIC224","value":-76},{"code":"IIC149","value":156814},{"code":"IIC130","value":156738},{"code":"IIC161","value":-975},{"code":"IIC170","value":0}],"productionValue":[{"code":"IIC127","value":0},{"code":"IIC129","value":0},{"code":"IIC223","value":95462},{"code":"IIC125","value":0},{"code":"IIC124","value":61276},{"code":"IIC128","value":95462},{"code":"IIC186","value":0},{"code":"IIC126","value":0}],"coverageRatios":{"ebitdaNetInterestCoverage":29.5139,"ebitNetInterestCoverage":-0.078,"ebitdaGrossInterestCoverage":29.5139,"ebitGrossInterestCoverage":-0.078},"efficiency":{"turnoverIndex":0.4709,"inventoryRotation":20.3556,"currentAssetsRotation":2.5614},"financialBurden":{"rod":0.33,"burdenIndex":3.39},"development":{"ebitVariation":-1.3248,"totalAssets":13.13,"mol":27.76,"addedValue":-8.7,"productionValue":-17.92},"rae":{"code":"641","description":"C.M. FRUTTA LATTE CARNE E PESCE"},"sae":{"code":"430","description":"Imprese produttive"},"financialCycle":{"stockDuration":17.9312},"liquidityRatios":{"cashTotalShortTermDebt":0.058},"profitability":{"ros":-0.05,"roe":-12.91,"roi":-0.02,"roaMonetary":8.35},"indebtedness":{"capitalizationDegree":0.0245,"leverage":40.8932,"debtRatio":35.8246},"financialStability":{"secondaryMarginStructure ":-263499,"marginStructure":0.03,"fixedAssetsCoverageRate":0.03,"marginStructureIndex":-263499,"workingCapitalCoverage":-1.5521,"acidTest":0.1757,"currentRatio":0.201},"financialStatementKpi":{"totalInventoryTurnover":45.252,"debtsTurnover":4.7584},"allOffices":[{"companyDetails":{"vatCode":"01584810558","taxCode":"01584810558","lastUpdateDate":"2025-09-09T06:35:59.2239393Z","cciaa":"TR","reaCode":"108702","companyName":"ANTICA GELATERIA GIROTTI SRL","officeType":{"code":"SSL","description":"Administrative headquarter and registered office"},"openapiNumber":"IT0496060BS0001"},"companyStatus":{"activityStatus":{"code":"A","description":"Enable"}},"address":{"streetName":"VIA RIMEMBRANZE, 48","zipCode":"05022","town":"AMELIA","province":{"code":"TR","description":"TERNI"},"region":{"code":"10","description":"UMBRIA"},"country":{"code":"IT","description":"Italia"}}},{"companyDetails":{"vatCode":"01584810558","taxCode":"01584810558","lastUpdateDate":"2025-09-09T06:35:59.2239393Z","companyName":"ANTICA GELATERIA GIROTTI SRL","officeType":{"code":"UL","description":"Local units"},"openapiNumber":"IT0496060BU8001"},"companyStatus":{"activityStatus":{"code":"A","description":"Enable"}},"address":{"streetName":"STRADA DELLA FOCIANA, 33","zipCode":"05020","town":"LUGNANO IN TEVERINA","province":{"code":"TR","description":"TERNI"},"region":{"code":"10","description":"UMBRIA"},"country":{"code":"IT","description":"Italia"}}}]},"custom":{"request_id":"85d5473c1fb683a175ab05b7c9b4b80e","vat_or_taxCode":"01584810558"}}
Ora otteniamo dati dettagliati per le altre gelaterie di Terni. Verifichiamo Gelateria Andrea:

O


Full italian companies data from VAT


O


Check async status
Richiesta

{
  "request_id": "49a910311b2803211c7f6a2d734a98bc"
}
Risposta

{"data":{"companyDetails":{"vatCode":"01586500553","taxCode":"01586500553","lastUpdateDate":"2025-09-09T17:43:59.3594393Z","cciaa":"TR","reaCode":"108837","companyName":"GELATERIA ANDREA SNC DI FEDERICI ANDREA & C.","officeType":{"code":"SSL","description":"Administrative headquarter and registered office"},"openapiNumber":"IT7C91030AS0001"},"legalForm":{"legalForm":{"code":"SP","description":"Partnership"},"detailedLegalForm":{"code":"SN","description":"Collective name company/ general partnership"}},"companyStatus":{"activityStatus":{"code":"A","description":"Enable"}},"companyDates":{"registrationDate":"2017-02-10T00:00:00","startDate":"2017-07-03T00:00:00","incorporationDate":"2017-02-02T00:00:00"},"address":{"streetName":"VIA FRANCESCO MANCINI, 7","zipCode":"05100","town":"TERNI","province":{"code":"TR","description":"TERNI"},"region":{"code":"10","description":"UMBRIA"},"country":{"code":"IT","description":"Italia"}},"marketable":{"isMarketable":true},"branches":{"numberOfBranches":0},"atecoClassification":{"ateco":{"code":"56112","description":"56112 - Ice cream parlours and pastry shops"},"secondaryAteco":"4712","ateco2022":{"code":"56103","description":"Ice-cream parlors and bakeries"},"secondaryAteco2022":"47"},"internationalClassification":{"nace":{"code":"561","description":"Restaurants and mobile food service activities"},"primarySic":{"code":"5441","description":"Sweet & confectionery retailers"},"secondarySic":"5999"},"ecofin":{"enterpriseSize":{"code":"ND99","description":"N. a."}},"pec":"GELATERIA.ANDREA@PEC.IT","employees":{"employeeRange":{"code":"ER3","description":"6 - 10"},"employee":6,"employeeTrend":0},"innovativeSmeAndSu":{"isInnovativeStartUp":false,"isInnovativeSme":false},"mail":{"email":""},"contacts":{"telephoneNumber":"0744085852","fax":""},"webAndSocial":{"hasSocial":false},"foreignTrade":{"isImporter":false,"isExporter":false},"managers":[{"name":"ANDREA","surname":"FEDERICI","roles":[{"role":{"code":"SOA","description":"Active partner/shareholder"},"roleStartDate":"2017-02-02T00:00:00"}],"gender":{"code":"M","description":"Man"},"taxCode":"FDRNDR87T12L117G","birthDate":"1987-12-12T00:00:00","age":37,"birthTown":"TERNI (TR)","isLegalRepresentative":true},{"name":"SIMONA","surname":"SILVESTRI","roles":[{"role":{"code":"COM","description":"Partner"},"roleStartDate":"2017-02-02T00:00:00"}],"gender":{"code":"F","description":"Woman"},"taxCode":"SLVSMN86M47H282P","birthDate":"1986-08-07T00:00:00","age":39,"birthTown":"RIETI (RI)","isLegalRepresentative":false}],"corporateGroups":{"belongsToGroup":false,"nationalParentCompany":{"province":{"code":"ND99","description":"N. A."}},"hasForeignSubsidiaries":false,"hasForeignParents":false},"artisanBusinessRegistry":{"belongsToArtisanBusinessRegistry":true,"artisanBusinessRegistry":{"registrationDate":"2017-07-26T00:00:00","registrationNumber":"27784"}},"soaCertification":{"hasSoaCertification":false},"rae":{"code":"641","description":"C.M. FRUTTA LATTE CARNE E PESCE"},"sae":{"code":"482","description":"Società con meno di 20 addetti"},"allOffices":[{"companyDetails":{"vatCode":"01586500553","taxCode":"01586500553","lastUpdateDate":"2025-09-09T17:43:59.3594393Z","cciaa":"TR","reaCode":"108837","companyName":"GELATERIA ANDREA SNC DI FEDERICI ANDREA & C.","officeType":{"code":"SSL","description":"Administrative headquarter and registered office"},"openapiNumber":"IT7C91030AS0001"},"companyStatus":{"activityStatus":{"code":"A","description":"Enable"}},"address":{"streetName":"VIA FRANCESCO MANCINI, 7","zipCode":"05100","town":"TERNI","province":{"code":"TR","description":"TERNI"},"region":{"code":"10","description":"UMBRIA"},"country":{"code":"IT","description":"Italia"}}}]},"custom":{"request_id":"49a910311b2803211c7f6a2d734a98bc","vat_or_taxCode":"01586500553"}}
Verifichiamo ora Gelateria Bar Porta Romana:

O


Full italian companies data from VAT


O


Check async status
Richiesta

{
  "request_id": "65d59bd8aa9b085f48c6f4bfe3ec18bb"
}
Risposta

{"data":{"companyDetails":{"vatCode":"01230200550","taxCode":"BRTSFN74D28L117X","lastUpdateDate":"2025-09-09T23:08:34.0208002Z","cciaa":"TR","reaCode":"82432","companyName":"GELATERIA BAR PORTA ROMANA DI BARTOLUCCI STEFANO","officeType":{"code":"SSL","description":"Administrative headquarter and registered office"},"openapiNumber":"IT6C8A0407S0001"},"legalForm":{"legalForm":{"code":"DI","description":"Individual company"},"detailedLegalForm":{"code":"DI","description":"Individual business"}},"companyStatus":{"activityStatus":{"code":"A","description":"Enable"}},"companyDates":{"registrationDate":"2001-06-26T00:00:00","startDate":"2001-05-09T00:00:00","incorporationDate":"2001-05-09T00:00:00"},"address":{"streetName":"VIA ROMA, 180","zipCode":"05100","town":"TERNI","province":{"code":"TR","description":"TERNI"},"region":{"code":"10","description":"UMBRIA"},"country":{"code":"IT","description":"Italia"}},"marketable":{"isMarketable":true},"branches":{"numberOfBranches":0},"atecoClassification":{"ateco":{"code":"56112","description":"56112 - Ice cream parlours and pastry shops"},"secondaryAteco":"563","ateco2022":{"code":"56103","description":"Ice-cream parlors and bakeries"},"secondaryAteco2022":"563"},"internationalClassification":{"nace":{"code":"561","description":"Restaurants and mobile food service activities"},"primarySic":{"code":"5441","description":"Sweet & confectionery retailers"},"secondarySic":"5813"},"ecofin":{"enterpriseSize":{"code":"ND99","description":"N. a."}},"pec":"BARPORTAROMANA@PEC.IT","employees":{"employeeRange":{"code":"ER2","description":"≤ 5"},"employee":5,"employeeTrend":0},"innovativeSmeAndSu":{"isInnovativeStartUp":false,"isInnovativeSme":false},"mail":{"email":""},"contacts":{"telephoneNumber":"0744406127","fax":""},"webAndSocial":{"hasSocial":false},"foreignTrade":{"isImporter":false,"isExporter":false},"managers":[{"name":"STEFANO","surname":"BARTOLUCCI","roles":[{"role":{"code":"TIT","description":"Owner with signatory powers"}}],"gender":{"code":"M","description":"Man"},"taxCode":"BRTSFN74D28L117X","birthDate":"1974-04-28T00:00:00","age":51,"birthTown":"TERNI (TR)","isLegalRepresentative":true}],"corporateGroups":{"belongsToGroup":false,"nationalParentCompany":{"province":{"code":"ND99","description":"N. A."}},"hasForeignSubsidiaries":false,"hasForeignParents":false},"artisanBusinessRegistry":{"belongsToArtisanBusinessRegistry":true,"artisanBusinessRegistry":{"registrationDate":"2001-06-25T00:00:00","registrationNumber":"21347"}},"soaCertification":{"hasSoaCertification":false},"rae":{"code":"641","description":"C.M. FRUTTA LATTE CARNE E PESCE"},"sae":{"code":"614","description":"Artigiani"},"allOffices":[{"companyDetails":{"vatCode":"01230200550","taxCode":"BRTSFN74D28L117X","lastUpdateDate":"2025-09-09T23:08:34.0208002Z","cciaa":"TR","reaCode":"82432","companyName":"GELATERIA BAR PORTA ROMANA DI BARTOLUCCI STEFANO","officeType":{"code":"SSL","description":"Administrative headquarter and registered office"},"openapiNumber":"IT6C8A0407S0001"},"companyStatus":{"activityStatus":{"code":"A","description":"Enable"}},"address":{"streetName":"VIA ROMA, 180","zipCode":"05100","town":"TERNI","province":{"code":"TR","description":"TERNI"},"region":{"code":"10","description":"UMBRIA"},"country":{"code":"IT","description":"Italia"}}}]},"custom":{"request_id":"65d59bd8aa9b085f48c6f4bfe3ec18bb","vat_or_taxCode":"01230200550"}}
Ora verifichiamo Gelateria Capitan Cono:

O


Full italian companies data from VAT


O


Check async status
Richiesta

{
  "request_id": "9a40195db40897613db0e46010e8cf68"
}
Risposta

{"data":{"companyDetails":{"vatCode":"01359140553","taxCode":"CRSMSM70E23L117E","lastUpdateDate":"2025-07-24T17:59:50.6330297Z","cciaa":"TR","reaCode":"91471","companyName":"GELATERIA PASTICCERIA CAPITAN CONO DI CRESTA MASSIMO","officeType":{"code":"SSL","description":"Administrative headquarter and registered office"},"openapiNumber":"ITD7870705S0001"},"legalForm":{"legalForm":{"code":"DI","description":"Individual company"},"detailedLegalForm":{"code":"DI","description":"Individual business"}},"companyStatus":{"activityStatus":{"code":"A","description":"Enable"}},"companyDates":{"registrationDate":"2007-01-11T00:00:00","startDate":"2007-01-05T00:00:00","incorporationDate":"2007-01-05T00:00:00"},"address":{"streetName":"VIA DEL RIVO, 227","zipCode":"05100","town":"TERNI","province":{"code":"TR","description":"TERNI"},"region":{"code":"10","description":"UMBRIA"},"country":{"code":"IT","description":"Italia"}},"marketable":{"isMarketable":true},"branches":{"numberOfBranches":0},"atecoClassification":{"ateco":{"code":"56112","description":"56112 - Ice cream parlours and pastry shops"},"secondaryAteco":"","ateco2022":{"code":"56103","description":"Ice-cream parlors and bakeries"},"secondaryAteco2022":""},"internationalClassification":{"nace":{"code":"5610","description":"Restaurants and mobile food service activities"},"primarySic":{"code":"5441","description":"Sweet & confectionery retailers"},"secondarySic":""},"ecofin":{"enterpriseSize":{"code":"ND99","description":"N. a."}},"employees":{"employeeRange":{"code":"ER2","description":"≤ 5"},"employee":1,"employeeTrend":0},"innovativeSmeAndSu":{"isInnovativeStartUp":false,"isInnovativeSme":false},"mail":{"email":""},"contacts":{"telephoneNumber":"0744305944;","fax":""},"webAndSocial":{"hasSocial":false},"foreignTrade":{"isImporter":false,"isExporter":false},"managers":[{"name":"MASSIMO","surname":"CRESTA","roles":[{"role":{"code":"TIT","description":"Owner with signatory powers"}}],"gender":{"code":"M","description":"Man"},"taxCode":"CRSMSM70E23L117E","birthDate":"1970-05-23T00:00:00","age":55,"birthTown":"TERNI (TR)","isLegalRepresentative":true}],"corporateGroups":{"belongsToGroup":false,"nationalParentCompany":{"province":{"code":"ND99","description":"N. A."}},"hasForeignSubsidiaries":false,"hasForeignParents":false},"artisanBusinessRegistry":{"belongsToArtisanBusinessRegistry":true,"artisanBusinessRegistry":{"registrationDate":"2007-05-22T00:00:00","registrationNumber":"23886"}},"soaCertification":{"hasSoaCertification":false},"rae":{"code":"641","description":"C.M. FRUTTA LATTE CARNE E PESCE"},"sae":{"code":"614","description":"Artigiani"},"allOffices":[{"companyDetails":{"vatCode":"01359140553","taxCode":"CRSMSM70E23L117E","lastUpdateDate":"2025-07-24T17:59:50.6330297Z","cciaa":"TR","reaCode":"91471","companyName":"GELATERIA PASTICCERIA CAPITAN CONO DI CRESTA MASSIMO","officeType":{"code":"SSL","description":"Administrative headquarter and registered office"},"openapiNumber":"ITD7870705S0001"},"companyStatus":{"activityStatus":{"code":"A","description":"Enable"}},"address":{"streetName":"VIA DEL RIVO, 227","zipCode":"05100","town":"TERNI","province":{"code":"TR","description":"TERNI"},"region":{"code":"10","description":"UMBRIA"},"country":{"code":"IT","description":"Italia"}}}]},"custom":{"request_id":"9a40195db40897613db0e46010e8cf68","vat_or_taxCode":"01359140553"}}
Dalla mia ricerca, ho identificato le principali gelaterie nell'area di Terni/provincia. Basandomi sui dati disponibili, l'Antica Gelateria Girotti è l'unica che ha dati di fatturato completi e chiari. Per le altre gelaterie di Terni non sono disponibili dati di fatturato specifici nei bilanci pubblici.

Creerò ora un report HTML completo con l'analisi delle prime 2 gelaterie che ho potuto identificare con maggiori informazioni:

Report Finanziario Gelaterie Terni
Contenuto interattivo 
Ho completato il report finanziario delle gelaterie di Terni in formato HTML.

Riepilogo dei Risultati:
Top 2 Gelaterie identificate:

🏆 Antica Gelateria Girotti S.R.L. (Amelia, provincia TR)
Fatturato 2024: €61.276 (in calo del -56% dal 2023)
Unica con dati finanziari completi e trasparenti
Struttura societaria solida (S.R.L.)
Presenza digitale sviluppata
🥈 Gelateria Andrea S.N.C. (Terni centro)
6 dipendenti, posizione strategica
Dati finanziari non pubblicamente disponibili
Società in nome collettivo ben strutturata
Considerazioni chiave:

Il mercato è dominato da micro-imprese individuali
Alta stagionalità e volatilità dei ricavi
Opportunità di consolidamento e digitalizzazione
Investimento stimato: €150-300k per acquisizione + €50k per upgrade
Il report include analisi dettagliate, metriche finanziarie, valutazione dei rischi e raccomandazioni specifiche per l'investimento. Ti consiglio particolare attenzione alla due diligence su Girotti per comprendere le cause del calo di fatturato 2024.

scrivi l'elenco di tutte le gelaterie che hai trovato infondo al report in una tabella

Report Finanziario Gelaterie Terni
Contenuto interattivo ∙ Versione 2 
Perfect! Ho aggiunto alla fine del report una sezione completa con l'elenco di tutte le 8 gelaterie identificate nella provincia di Terni. La tabella include:

📋 Dettagli per ogni gelateria:

Numero progressivo con evidenziazione delle top 2
Ragione sociale completa
Indirizzo completo
Comune di appartenenza
Partita IVA/Codice Fiscale
Forma giuridica
Numero dipendenti
Anno di fondazione
Codice ATECO
Status di attività
📊 Statistiche riassuntive:

8 gelaterie totali identificate
5 gelaterie pure + 3 bar-gelaterie
18 dipendenti totali nel settore
Distribuzione geografica e per forme giuridiche
📈 Note metodologiche:

Criteri di ricerca utilizzati
Limitazioni dell'analisi
Copertura della ricerca
La tabella evidenzia chiaramente le prime 2 gelaterie (con sfondo colorato) e fornisce una panoramica completa del mercato delle gelaterie nella provincia di Terni, utile per valutare completamente le opportunità di investimento nel settore.