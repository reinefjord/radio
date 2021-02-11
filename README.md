# radio

Tiny internet radio player.

Add stations in `~/.stations.json`:

```json
{
    "stations": [
        {
            "url": "http://somafm.com/defcon130.pls",
            "name": "SomaFM - DEF CON Radio",
            "keywords": ["somafm", "defcon"]
        },
        {
            "url": "http://somafm.com/cliqhop130.pls",
            "name": "SomaFM - cliqhop idm",
            "keywords": ["somafm", "cliqhop", "idm"]
        },
        {
            "url": "http://wbgo.streamguys.net/listen.pls",
            "name": "WBGO",
            "keywords": ["wbgo", "jazz"]
        }
    ]
}
```

Play by executing `radio` with a (partial or full) keyword:

```
$ radio def
-> playing SomaFM - DEF CON Radio
Playing: http://somafm.com/defcon130.pls

Playing: http://ice2.somafm.com/defcon-128-aac
 (+) Audio --aid=1 (aac 2ch 44100Hz)
AO: [pulse] 44100Hz stereo 2ch float
A: 00:00:06 / 00:00:11 (56%) Cache:  5s+310KB
File tags:
 icy-title: MMOTHS - For Her (feat. Young & Sick)
A: 00:02:50 / 00:02:55 (97%) Cache:  5s+342KB
```

Keywords matching multiple stations will print the matches:

```
$ radio soma
multiple matches:
SomaFM - DEF CON Radio
SomaFM - cliqhop idm
```

No keyword will match all stations:

```
$ radio
multiple matches:
SomaFM - DEF CON Radio
SomaFM - cliqhop idm
WBGO
```


## Dependencies

* mpv
* jq
