Get the metadata and tracklist for an album on Last.fm using the album name or a MusicBrainz ID.

No authentication required.

## Parameters

| Method | Type | Default | Required | Description 
| ------ | ---- | ------- | -------- | -----------
| `artist` | [string][string] | `none` | :white_check_mark: \* | The artist which's album should be fetched.
| `album` | [string][string] | `none` | :white_check_mark: \* | The album that should be fetched.
| `mbid` | [string][string] | `none` | :negative_squared_cross_mark: | The album's MusicBrainz ID.
| `autocorrect` | [number][number] | 0 | :negative_squared_cross_mark: | Automatically corrects any mistakes in the artist's name.
| `lang` | [string][string] | en | :negative_squared_cross_mark: | The language which will be used in the response for biography. Requires an ISO 639 alpha-1 code.
| `username` | [string][string] | `none` | :negative_squared_cross_mark: | The user in the context of the request. If submitted, will provide information about the user for the requested album.
| `api_key` | [key][key] | `none` | :white_check_mark: | A Last.fm API key.

\* Required unless you are using a MusicBrainz ID for the album.

## Responses

Errors:

- 2 : Invalid service - This service does not exist
- 3 : Invalid Method - No method with that name in this package
- 4 : Authentication Failed - You do not have permissions to access the service
- 5 : Invalid format - This service doesn't exist in that format
- 6 : Invalid parameters - Your request is missing a required parameter
- 7 : Invalid resource specified
- 8 : Operation failed - Something else went wrong
- 9 : Invalid session key - Please re-authenticate
- 10 : Invalid API key - You must be granted a valid key by last.fm
- 11 : Service Offline - This service is temporarily offline. Try again later.
- 13 : Invalid method signature supplied
- 16 : There was a temporary error processing your request. Please try again
- 26 : Suspended API key - Access for your account has been suspended, please contact Last.fm
- 29 : Rate limit exceeded - Your IP has made too many requests in a short period

!!! Warning
    This API call returns 200 OK HTTP status codes even when the response contains an error.
    
## Attributes

duration - in seconds

## Examples

??? note "Example response"

    | Parameter | Value         |
    | --------- | ------------- |
    | artist    | Metallica     |
    | album     | Metallica     |
    | lang      | de            |
    | api_key   | YOUR_API_KEY  |
    | format    | json          |

    HTTP status: `200 OK`

    ```
    https://ws.audioscrobbler.com/2.0/?method=album.getInfo&artist=Metallica&album=Metallica&lang=de&api_key=YOUR_API_KEY&format=json
    ```

    ```json
    {
    "album": {
        "name": "Metallica",
        "artist": "Metallica",
        "mbid": "6e729716-c0eb-3f50-a740-96ac173be50d",
        "url": "https://www.last.fm/music/Metallica/Metallica",
        "image": [
        {
            "#text": "https://lastfm.freetls.fastly.net/i/u/34s/dd396f972110a303a4970a9b9daaf719.png",
            "size": "small"
        },
        {
            "#text": "https://lastfm.freetls.fastly.net/i/u/64s/dd396f972110a303a4970a9b9daaf719.png",
            "size": "medium"
        },
        {
            "#text": "https://lastfm.freetls.fastly.net/i/u/174s/dd396f972110a303a4970a9b9daaf719.png",
            "size": "large"
        },
        {
            "#text": "https://lastfm.freetls.fastly.net/i/u/300x300/dd396f972110a303a4970a9b9daaf719.png",
            "size": "extralarge"
        },
        {
            "#text": "https://lastfm.freetls.fastly.net/i/u/300x300/dd396f972110a303a4970a9b9daaf719.png",
            "size": "mega"
        },
        {
            "#text": "https://lastfm.freetls.fastly.net/i/u/300x300/dd396f972110a303a4970a9b9daaf719.png",
            "size": ""
        }
        ],
        "listeners": "1290895",
        "playcount": "29408961",
        "tracks": {
        "track": [
            {
            "name": "Enter Sandman",
            "url": "https://www.last.fm/music/Metallica/_/Enter+Sandman",
            "duration": "382",
            "@attr": {
                "rank": "1"
            },
            "streamable": {
                "#text": "0",
                "fulltrack": "0"
            },
            "artist": {
                "name": "Metallica",
                "mbid": "65f4f0c5-ef9e-490c-aee3-909e7ae6b2ab",
                "url": "https://www.last.fm/music/Metallica"
            }
            },
            {
            "name": "Sad but True",
            "url": "https://www.last.fm/music/Metallica/_/Sad+but+True",
            "duration": "324",
            "@attr": {
                "rank": "2"
            },
            "streamable": {
                "#text": "0",
                "fulltrack": "0"
            },
            "artist": {
                "name": "Metallica",
                "mbid": "65f4f0c5-ef9e-490c-aee3-909e7ae6b2ab",
                "url": "https://www.last.fm/music/Metallica"
            }
            },
            {
            "name": "Holier Than Thou",
            "url": "https://www.last.fm/music/Metallica/_/Holier+Than+Thou",
            "duration": "227",
            "@attr": {
                "rank": "3"
            },
            "streamable": {
                "#text": "0",
                "fulltrack": "0"
            },
            "artist": {
                "name": "Metallica",
                "mbid": "65f4f0c5-ef9e-490c-aee3-909e7ae6b2ab",
                "url": "https://www.last.fm/music/Metallica"
            }
            },
            {
            "name": "The Unforgiven",
            "url": "https://www.last.fm/music/Metallica/_/The+Unforgiven",
            "duration": "386",
            "@attr": {
                "rank": "4"
            },
            "streamable": {
                "#text": "0",
                "fulltrack": "0"
            },
            "artist": {
                "name": "Metallica",
                "mbid": "65f4f0c5-ef9e-490c-aee3-909e7ae6b2ab",
                "url": "https://www.last.fm/music/Metallica"
            }
            },
            {
            "name": "Wherever I May Roam",
            "url": "https://www.last.fm/music/Metallica/_/Wherever+I+May+Roam",
            "duration": "402",
            "@attr": {
                "rank": "5"
            },
            "streamable": {
                "#text": "0",
                "fulltrack": "0"
            },
            "artist": {
                "name": "Metallica",
                "mbid": "65f4f0c5-ef9e-490c-aee3-909e7ae6b2ab",
                "url": "https://www.last.fm/music/Metallica"
            }
            },
            {
            "name": "Don't Tread on Me",
            "url": "https://www.last.fm/music/Metallica/_/Don%27t+Tread+on+Me",
            "duration": "239",
            "@attr": {
                "rank": "6"
            },
            "streamable": {
                "#text": "0",
                "fulltrack": "0"
            },
            "artist": {
                "name": "Metallica",
                "mbid": "65f4f0c5-ef9e-490c-aee3-909e7ae6b2ab",
                "url": "https://www.last.fm/music/Metallica"
            }
            },
            {
            "name": "Through the Never",
            "url": "https://www.last.fm/music/Metallica/_/Through+the+Never",
            "duration": "241",
            "@attr": {
                "rank": "7"
            },
            "streamable": {
                "#text": "0",
                "fulltrack": "0"
            },
            "artist": {
                "name": "Metallica",
                "mbid": "65f4f0c5-ef9e-490c-aee3-909e7ae6b2ab",
                "url": "https://www.last.fm/music/Metallica"
            }
            },
            {
            "name": "Nothing Else Matters",
            "url": "https://www.last.fm/music/Metallica/_/Nothing+Else+Matters",
            "duration": "341",
            "@attr": {
                "rank": "8"
            },
            "streamable": {
                "#text": "0",
                "fulltrack": "0"
            },
            "artist": {
                "name": "Metallica",
                "mbid": "65f4f0c5-ef9e-490c-aee3-909e7ae6b2ab",
                "url": "https://www.last.fm/music/Metallica"
            }
            },
            {
            "name": "Of Wolf and Man",
            "url": "https://www.last.fm/music/Metallica/_/Of+Wolf+and+Man",
            "duration": "256",
            "@attr": {
                "rank": "9"
            },
            "streamable": {
                "#text": "0",
                "fulltrack": "0"
            },
            "artist": {
                "name": "Metallica",
                "mbid": "65f4f0c5-ef9e-490c-aee3-909e7ae6b2ab",
                "url": "https://www.last.fm/music/Metallica"
            }
            },
            {
            "name": "The God That Failed",
            "url": "https://www.last.fm/music/Metallica/_/The+God+That+Failed",
            "duration": "305",
            "@attr": {
                "rank": "10"
            },
            "streamable": {
                "#text": "0",
                "fulltrack": "0"
            },
            "artist": {
                "name": "Metallica",
                "mbid": "65f4f0c5-ef9e-490c-aee3-909e7ae6b2ab",
                "url": "https://www.last.fm/music/Metallica"
            }
            },
            {
            "name": "My Friend of Misery",
            "url": "https://www.last.fm/music/Metallica/_/My+Friend+of+Misery",
            "duration": "407",
            "@attr": {
                "rank": "11"
            },
            "streamable": {
                "#text": "0",
                "fulltrack": "0"
            },
            "artist": {
                "name": "Metallica",
                "mbid": "65f4f0c5-ef9e-490c-aee3-909e7ae6b2ab",
                "url": "https://www.last.fm/music/Metallica"
            }
            },
            {
            "name": "The Struggle Within",
            "url": "https://www.last.fm/music/Metallica/_/The+Struggle+Within",
            "duration": "231",
            "@attr": {
                "rank": "12"
            },
            "streamable": {
                "#text": "0",
                "fulltrack": "0"
            },
            "artist": {
                "name": "Metallica",
                "mbid": "65f4f0c5-ef9e-490c-aee3-909e7ae6b2ab",
                "url": "https://www.last.fm/music/Metallica"
            }
            }
        ]
        },
        "tags": {
        "tag": [
            {
            "name": "albums I own",
            "url": "https://www.last.fm/tag/albums+I+own"
            },
            {
            "name": "heavy metal",
            "url": "https://www.last.fm/tag/heavy+metal"
            },
            {
            "name": "metal",
            "url": "https://www.last.fm/tag/metal"
            },
            {
            "name": "thrash metal",
            "url": "https://www.last.fm/tag/thrash+metal"
            },
            {
            "name": "hard rock",
            "url": "https://www.last.fm/tag/hard+rock"
            }
        ]
        },
        "wiki": {
        "published": "06 Oct 2008, 13:22",
        "summary": "Metallica ist das fünfte Studioalbum der gleichnamigen US-amerikanischen Heavy-Metal-Band Metallica. Es erschien am 12. August 1991 bei Elektra Records und wird aufgrund seines schlichten, fast komplett schwarzen Covers häufig The Black Album genannt. Das hauptsächlich vom Kanadier Bob Rock produzierte Album markierte einen Wendepunkt in der musikalischen Entwicklung der Band. Nachdem die Lieder zuvor immer länger und progressiver geworden waren, schrieb die Band nun einfacher arrangierte, kürzere und eingängigere Songs. <a href=\"https://www.last.fm/music/Metallica/Metallica\">Read more on Last.fm</a>.",
        "content": "Metallica ist das fünfte Studioalbum der gleichnamigen US-amerikanischen Heavy-Metal-Band Metallica. Es erschien am 12. August 1991 bei Elektra Records und wird aufgrund seines schlichten, fast komplett schwarzen Covers häufig The Black Album genannt. Das hauptsächlich vom Kanadier Bob Rock produzierte Album markierte einen Wendepunkt in der musikalischen Entwicklung der Band. Nachdem die Lieder zuvor immer länger und progressiver geworden waren, schrieb die Band nun einfacher arrangierte, kürzere und eingängigere Songs.\n\nMit weltweit über 28 Millionen verkauften Einheiten, davon über 16 Millionen in den USA, ist Metallica bis heute das meistverkaufte Metal-Album. In zehn Ländern erreichte es Platz eins der jeweiligen Albumcharts. 1992 erhielten Metallica den Grammy Award in der Kategorie Best Metal Performance. <a href=\"https://www.last.fm/music/Metallica/Metallica\">Read more on Last.fm</a>. User-contributed text is available under the Creative Commons By-SA License; additional terms may apply."
        }
    }
    }

    ```

??? warning "Example response of an artist/album that doesnt exist"
    HTTP status: `200 OK`

    ```
    https://ws.audioscrobbler.com/2.0/?method=album.getinfo&api_key=YOUR_API_KEY&artist=metallica&album=albumthatdoesnotexist&format=json
    ```
    ```json
    {
        "error": 6,
        "message": "Album not found",
        "links": []
    }   
    ```

[string]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String
[number]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number
[key]: https://www.last.fm/api/account/create