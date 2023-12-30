# be-nesting

Turn:

```html
<span be-nesting='
{
    "model": {
        "person": {
            "name":{
                "firstName": "Martha",
                "lastName": "Washington"
            },
            "address" {
                "gpsCoordinates": {
                    "latitude": 12345678.90
                }
            }
        }
    },
    "path": "person.address.gpsCoordinates.latitude"
}
'></span>
```

generates:

```html
<span be-nesting='...' itemscope itemprop=person>
    <span itemscope itemprop=address>
        <span itemscope itemprop=gpsCoordinates>
            <data value=12345678.90>12,345,678.90</data>
        </span>
    </span>
</span>
```