---
title: RTB Интеграция
description: 
layout: libdoc/page

order: 95
---
* 
{:toc}

## RTB Интеграция

DSP Адаптер по умолчанию работает с следующими BidRequest/BidResponse.
В примере  OpenRTB BidRequest содержит два Imp объекта, один Banner и один Native c plcmtcnt = 4, по спецификации в ответе OpenRTB BidResponse ожидается 5 объектов Bid, 1 для баннера и 4 для нативной рекламы.

Пример страницы с рекламой https://demo.rtblab.online/

## Default BidRequest
```json
{
  "id": "97e514d1-6fb6-4217-be3f-c65449b19a40",
  "imp": [
    {
      "id": "40dc031a-5cf9-4d26-b72f-ebcf01c46c23",
      "banner": {
        "w": 728,
        "h": 90
      }
    },
    {
      "id": "40dc031a-5cf9-4d26-b72f-ebcf01c46c26",
      "native": {
        "request": "{\"ver\":\"1.2\",\"plcmtcnt\":4,\"assets\":[{\"id\":0,\"required\":1,\"title\":{\"len\":90}},{\"id\":0,\"required\":1,\"img\":{\"type\":3,\"wmin\":150,\"hmin\":150}},{\"id\":0,\"required\":1,\"data\":{\"type\":2}}]}"
      }
    }
  ],
  "site": {
    "id": "b1d69207-2ef4-4467-88bc-ce23a7759789",
    "cattax": 4
  },
  "device": {
    "geo": {},
    "ua": "Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/119.0.0.0 Safari/537.36",
    "ip": "127.0.0.1",
    "ipv6": "127.0.0.1",
    "devicetype": 2,
    "os": "Linux"
  }
}
```

## Default BidResponse
```json
{
	"id": "97e514d1-6fb6-4217-be3f-c65449b19a40",
	"seatbid": [
		{
			"bid": [
				{
					"id": "26165ae2-0899-4387-b58d-c77fd76eeebf",
					"impid": "40dc031a-5cf9-4d26-b72f-ebcf01c46c23",
					"price": 1.4643857993176388,
					"adm": "<a href=\"https://yandex.ru?dsp=dsp-1\"><img src=\"https://demo.rtblab.online/banners/728x90/06.gif\"/></a>",
					"mtype": 1
				},
				{
					"id": "2d9da877-818d-4b0a-b264-6a0d6207dc70",
					"impid": "40dc031a-5cf9-4d26-b72f-ebcf01c46c26",
					"price": 0.859415560592452,
					"adm": "{\"ver\":\"1.2\",\"assets\":[{\"title\":{\"text\":\"[DSP-1] Man finds hidden house with no doors or windows - He goes inside and immediately calls the police\"}},{\"img\":{\"type\":3,\"url\":\"https://demo.rtblab.online/native/014.png\"}},{\"data\":{\"type\":2,\"value\":\"\"}}],\"link\":{\"url\":\"https://Storytohear.com?dsp=dsp-1\"}}",
					"mtype": 4
				},
				{
					"id": "53b81127-b117-47fd-94a4-ab2b1103c40d",
					"impid": "40dc031a-5cf9-4d26-b72f-ebcf01c46c26",
					"price": 0.9353240627502382,
					"adm": "{\"ver\":\"1.2\",\"assets\":[{\"title\":{\"text\":\"[DSP-1] Empty Alaska Cruise Cabins Come with Tiny Price Tags\"}},{\"img\":{\"type\":3,\"url\":\"https://demo.rtblab.online/native/018.jpg\"}},{\"data\":{\"type\":2,\"value\":\"\"}}],\"link\":{\"url\":\"https://Gosearches.net?dsp=dsp-1\"}}",
					"mtype": 4
				},
				{
					"id": "e2c625d8-64e2-430a-9a02-590d5f4dd01a",
					"impid": "40dc031a-5cf9-4d26-b72f-ebcf01c46c26",
					"price": 1.3627864370601337,
					"adm": "{\"ver\":\"1.2\",\"assets\":[{\"title\":{\"text\":\"[DSP-1] Play this game for 1 minute and see why everyone is addicted.\"}},{\"img\":{\"type\":3,\"url\":\"https://demo.rtblab.online/native/011.jpg\"}},{\"data\":{\"type\":2,\"value\":\"\"}}],\"link\":{\"url\":\"https://Strategycombat.com?dsp=dsp-1\"}}",
					"mtype": 4
				},
				{
					"id": "575bf3e1-9fcd-4a3a-911b-002873dcffa7",
					"impid": "40dc031a-5cf9-4d26-b72f-ebcf01c46c26",
					"price": 1.1293271876333448,
					"adm": "{\"ver\":\"1.2\",\"assets\":[{\"title\":{\"text\":\"[DSP-1] Here Are 7 Legal Discounts Seniors Get Only If They Ask\"}},{\"img\":{\"type\":3,\"url\":\"https://demo.rtblab.online/native/006.jpg\"}},{\"data\":{\"type\":2,\"value\":\"\"}}],\"link\":{\"url\":\"https://Nationalpenny.com?dsp=dsp-1\"}}",
					"mtype": 4
				}
			],
			"seat": "creatives.com"
		}
	]
}
```

