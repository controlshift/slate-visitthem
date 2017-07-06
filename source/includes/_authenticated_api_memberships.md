# Memberships

Members of Congress are represented by memberships.  A membership record includes specific fields for faction, chamber, district, etc.; as well as personal information about the legislator, offices, and upcoming events.

## Find by area

```json
{
  "memberships": [
    {
      "id": 1396,
      "faction": "Democrat",
      "legislature": "US House of Representatives",
      "legislative_period": "115th Congress",
      "district_abbreviation": "OR-1",
      "district_name": "OR Congressional District 1",
      "start_date": "2017-01-03",
      "end_date": "2019-01-03",
      "us_senate_class": null,
      "us_senate_state_rank": null,
      "url": "http://bonamici.house.gov",
      "address": "439 Cannon HOB; Washington DC 20515-3701",
      "phone": "202-225-0855",
      "fax": "202-225-9497",
      "rss_url": "http://bonamici.house.gov/rss.xml",
      "contact_form_url": null,
      "person": {
        "id": 1408,
        "official_full_name": "Suzanne Bonamici",
        "first_name": "Suzanne",
        "middle_name": null,
        "last_name": "Bonamici",
        "birth_date": "1954-10-14",
        "bioguide_id": "B001278",
        "lis_id": null,
        "govtrack_id": "412501",
        "opensecrets_id": null,
        "votesmart_id": "59641",
        "wikidata_id": "Q45946",
        "google_entity_id": "kg:/m/02q453x",
        "photo_url": "/photos/avatar/missing.png",
        "facebook": "congresswomanbonamici",
        "twitter": "RepBonamici"
      },
      "offices": [
        {
          "latitude": "45.4900502",
          "longitude": "-122.8078224",
          "suite": "Suite 220",
          "building": "",
          "address": "12725 SW Millikan Way",
          "locality": "Beaverton",
          "region": "OR",
          "postal_code": "97005",
          "country": "US",
          "hours": "Monday-Friday 9:00AM-5:00PM",
          "phone": "503-469-6010",
          "time_zone": "America/Los_Angeles",
          "source_id": "B001278-beaverton"
        }
      ],
      "events": [
        {
          "id": 2159,
          "start_at": "2017-07-06T14:00:00-07:00",
          "end_at": "2017-07-06T15:00:00-07:00",
          "kind": "town_hall",
          "source": "facebook",
          "source_url": null,
          "time_zone": "America/Los_Angeles",
          "notes": "Join Senator Ron Wyden and Congresswoman Suzanne Bonamici for a Town Hall meeting in Beaverton!\n\nTown Hall meetings provide an opportunity to discuss issues, answer questions, and gather ideas.\n\nBeaverton Town Hall Meeting\nDate: Thursday, July 6, 2017\nTime: 2:00pm\nLocation: Conestoga Recreation & Aquatic Center, 9985 SW 125th Ave, Beaverton\n\nTo stay up to date on future town hall meetings, please subscribe to the Bonamici Bulletin monthly e-newsletter by clicking here: https://bonamici.house.gov/contact-me/newsletter.",
          "facebook_id": "142710249637356",
          "town_hall_project_id": "-Knu2PDPK2S9wqA7bmyl",
          "latitude": "45.448749389702",
          "longitude": "-122.80626280071",
          "place": "THPRD Conestoga Recreation and Aquatic Center",
          "address": "9985 SW 125th Ave",
          "locality": "Beaverton",
          "region": "OR",
          "country": "US",
          "postal_code": "97008"
        }
      ]
    }
  ]
}
```

Find all memberships for a given area.

`GET /api/v1/memberships/for_area/<area abbreviation>`

Where `<area abbreviation>` is a State abbreviation (e.g.: NY, CA) or a Congressional District abbreviation (e.g.: IL-1, NJ-2).

## Find by proximity to a geographical point

```json
{
  "memberships": [
    {
      "id": 1094,
      "faction": "Democrat",
      "legislature": "US Senate",
      "legislative_period": "115th Congress",
      "district_abbreviation": "OR",
      "district_name": "Oregon",
      "start_date": "2017-01-03",
      "end_date": "2019-01-03",
      "us_senate_class": 2,
      "us_senate_state_rank": "junior",
      "url": "https://www.merkley.senate.gov",
      "address": "313 Hart Senate Office Building Washington DC 20510",
      "phone": "202-224-3753",
      "fax": "202-228-3997",
      "rss_url": "http://www.merkley.senate.gov/rss/",
      "contact_form_url": null,
      "person": {
        "id": 1106,
        "official_full_name": "Jeff Merkley",
        "first_name": "Jeff",
        "middle_name": null,
        "last_name": "Merkley",
        "birth_date": "1956-10-24",
        "bioguide_id": "M001176",
        "lis_id": "S322",
        "govtrack_id": "412325",
        "opensecrets_id": null,
        "votesmart_id": "23644",
        "wikidata_id": "Q1368405",
        "google_entity_id": "kg:/m/026k60f",
        "photo_url": "//d4o7gh77lka9h.cloudfront.net/people/photos/1106/avatar/M001176.jpg?1498867309",
        "facebook": "jeffmerkley",
        "twitter": "SenJeffMerkley"
      },
      "offices": [
        {
          "latitude": "45.5160884",
          "longitude": "-122.6748937",
          "suite": "Ste. 1400",
          "building": "",
          "address": "121 SW. Salmon St.",
          "locality": "Portland",
          "region": "OR",
          "postal_code": "97204",
          "country": "US",
          "hours": "",
          "phone": "503-326-3386",
          "time_zone": "America/Los_Angeles",
          "source_id": "M001176-portland",
          "distance": 22.755
        },
        ...
      ],
      "events": [
        {
          "id": 2436,
          "start_at": "2017-07-06T17:30:00-07:00",
          "end_at": null,
          "kind": "town_hall",
          "source": "town_hall_project",
          "source_url": null,
          "time_zone": "America/Los_Angeles",
          "notes": null,
          "facebook_id": null,
          "town_hall_project_id": "-Ko9N44HaDg6kCxwRCr-",
          "latitude": "45.45449",
          "longitude": "-123.820823",
          "place": "East Elementary School Gym",
          "address": "3905 Alder Lane",
          "locality": "Tillamook",
          "region": "OR",
          "country": "US",
          "postal_code": "97141",
          "distance": 77.906
        },
        ...
      ]
    },
    ...
  ]
}
```

> JSON response also includes the `distance` field for offices and events, with the distance measured in miles to the geographic point provided on the request.

`GET /api/v1/memberships/local?longitude=<longitude>&latitude=<latitude>&region=<region>&country=<country>`

Where:

* `<longitude>` is the longitude expressed in decimal degrees (e.g.: -122.2134)
* `<latitude>` is the latitude expressed in decimal degrees (e.g.: 45.4546)
* `<region>` is the state abbreviation (e.g.: OR)
* `<country>` is the ISO 3166-1 country abbreviation (e.g.: US)
