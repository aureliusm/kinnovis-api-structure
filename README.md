# Kinnovis API structure

Below is the JSON structure for API endpoint that will serve the Frontend (FE) to be able to load correct component with correct data and translations.

- `status` let's the FE know if all went fine and data is good
- `locale` let's the FE know what locale was used to generate the response
- `data` holds an array of fields. Each field has a `type` which let's the FE know which component to load. It also holds a `label` which is translated according to the requested locale. Depending on the type, filters also provide `options` for the FE to be able to load the component. Options have a `value` and a `label` which can also be translated on the BE.

```
{
    "status": "OK",
    "locale": "en",
    "data": {
        "search": {
            "type": "fulltext-search",
            "label": "Search"
        },
        "location": {
            "type": "multiselect",
            "label": "Location",
            "options": [
                {
                    "value": "Storeroom Innsbruck",
                    "label": "Storeroom Innsbruck"
                },
                {
                    "value": "Storeroom Wien",
                    "label": "Storeroom Wien"
                },
                {
                    "value": "Storeroom Graz",
                    "label": "Storeroom Graz"
                }
            ]
        },
        "unitTypeSize": {
            "type": "multiselect",
            "label": "Unit type size",
            "options": [
                {
                    "value": 2,
                    "label": "2 m<sup>2</sup>"
                },
                {
                    "value": 5,
                    "label": "5 m<sup>2</sup>"
                },
                {
                    "value": 8,
                    "label": "8 m<sup>2</sup>"
                },
                {
                    "value": 10,
                    "label": "10 m<sup>2</sup>"
                },
                {
                    "value": 30,
                    "label": "30 m<sup>2</sup>"
                },
                {
                    "value": 50,
                    "label": "50 m<sup>2</sup>"
                },
                {
                    "value": 100,
                    "label": "100 m<sup>2</sup>"
                },
                {
                    "value": 160,
                    "label": "160 m<sup>2</sup>"
                }
            ]
        },
        "status": {
            "type": "multiselect",
            "label": "Status",
            "options": [
                {
                    "value": "vacant",
                    "label": "Vacant"
                },
                {
                    "value": "maintenance",
                    "label": "Maintenance"
                },
                {
                    "value": "blocked",
                    "label": "Blocked"
                }
            ]
        }
    }
}
```
