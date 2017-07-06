# People

A person record references an individual, who may be associated with multiple memberships (with only one of them being current).

## Lookup by external ID

```json
{
  "person": {
    "id": 1091,
    "official_full_name": "Bernard Sanders",
    "first_name": "Bernard",
    "middle_name": null,
    "last_name": "Sanders",
    "birth_date": "1941-09-08",
    "bioguide_id": "S000033",
    "lis_id": "S313",
    "govtrack_id": "400357",
    "opensecrets_id": null,
    "votesmart_id": "27110",
    "wikidata_id": "Q359442",
    "google_entity_id": "kg:/m/01_gbv",
    "photo_url": "//d4o7gh77lka9h.cloudfront.net/people/photos/1091/avatar/S000033.jpg?1498867301",
    "facebook": "senatorsanders",
    "twitter": "SenSanders"
  },
  "memberships": [
    {
      "id": 1079,
      "faction": "Independent",
      "legislature": "US Senate",
      "legislative_period": "115th Congress",
      "district_abbreviation": "VT",
      "district_name": "Vermont",
      "start_date": "2017-01-03",
      "end_date": "2019-01-03",
      "us_senate_class": 1,
      "us_senate_state_rank": "junior",
      "url": "https://www.sanders.senate.gov",
      "address": "332 Dirksen Senate Office Building Washington DC 20510",
      "phone": "202-224-5141",
      "fax": "202-228-0776",
      "rss_url": "http://www.sanders.senate.gov/rss/",
      "contact_form_url": null,
      "offices": [
        {
          "latitude": "44.4802081",
          "longitude": "-73.2130702",
          "suite": "3rd Floor",
          "building": "",
          "address": "1 Church St.",
          "locality": "Burlington",
          "region": "VT",
          "postal_code": "05401",
          "country": "US",
          "hours": "",
          "phone": "802-862-0697",
          "time_zone": "America/New_York",
          "source_id": "S000033-burlington"
        },
        ...
      ],
      "events": []
    }
  ]
}
```

Find a person by an external ID.

Memberships are ordered from most to less recent.

### HTTP Request

`GET /api/v1/people/find/<search_field>/<search_value>`

Where:

* `<search field>` is one of the supported external IDs:
  * bioguide: The alphanumeric ID for this legislator in the [Biographical Directory of the United States Congress](http://bioguide.congress.gov).
  * google_entity: The alphanumeric ID for this legislator in [Google Knowdlege Graph](https://developers.google.com/knowledge-graph/).
  * govtrack: The numeric ID for this legislator on [GovTrack.us](https://www.govtrack.us/) (stored as an integer).
  * lis: The alphanumeric ID for this legislator found in [Senate roll call votes](http://www.senate.gov/pagelayout/legislative/a_three_sections_with_teasers/votes.htm).
  * opensecrets: The alphanumeric ID for this legislator on [OpenSecrets.org](http://www.opensecrets.org/)
  * votesmart: The numeric ID for this legislator on [VoteSmart.org](https://votesmart.org/) (stored as an integer).
  * wikidata: The alphanumeric ID for this legislator on [Wikidata](https://www.wikidata.org).
* `<search_value>` is the legislator's external ID value.

<aside class="notice">Remember to URL encode the search_value as it may contain invalid characters.</aside>
