# Province, District and Village Data in Laos PDR (ຂໍ້ມູນ ບ້ານ, ເມຶອງ ແລະ ແຂວງ ໃນປະເທດລາວ)
ໃນ Repo ນີ້ປະກອບມີໄຟລ json ທີ່ເກັບມູນ ບ້ານ, ເມຶອງ ແລະ ແຂວງ ໃນປະເທດລາວ.

## JSON Schema
    
```json
{
  "$schema": "http://json-schema.org/draft-07/schema#",
  "type": "object",
  "properties": {
    "totalProvinces": {
      "type": "number"
    },
    "totalDistricts": {
      "type": "number"
    },
    "totalVillages": {
      "type": "number"
    },
    "provincesData": {
      "type": "array",
      "items": {
        "type": "object",
        "properties": {
          "provinceEngName": {
            "type": "string"
          },
          "provinceLaoName": {
            "type": "string"
          },
          "provinceCode": {
            "type": "string"
          },
          "totalDistricts": {
            "type": "number"
          },
          "districtsData": {
            "type": "array",
            "items": {
              "type": "object",
              "properties": {
                "districtEngName": {
                  "type": "string"
                },
                "districtLaoName": {
                  "type": "string"
                },
                "districtCode": {
                  "type": "string"
                },
                "totalVillages": {
                  "type": "number"
                },
                "villagesData": {
                  "type": "array",
                  "items": {
                    "type": "object",
                    "properties": {
                      "villageEngName": {
                        "type": "string"
                      },
                      "villageLaoName": {
                        "type": "string"
                      },
                      "villageCode": {
                        "type": "string"
                      }
                    },
                    "required": ["villageEngName", "villageLaoName", "villageCode"]
                  }
                }
              },
              "required": ["districtEngName", "districtLaoName", "districtCode", "totalVillages", "villagesData"]
            }
          }
        },
        "required": ["provinceEngName", "provinceLaoName", "provinceCode", "totalDistricts", "districtsData"]
      }
    }
  },
  "required": ["totalProvinces", "totalDistricts", "totalVillages", "provincesData"]
}
```


## ຕົວຢ່າງ:
```json
{
  "totalProvinces": 18, // number
  "totalDistricts": 148, // number
  "totalVillages": 9692, // number
  "provincesData": [ // Array<object>
    {
      "provinceEngName": "VIENTIANE CAPITAL", // string
      "provinceLaoName": "ນະຄອນຫຼວງວຽງຈັນ", // string
      "provinceCode": "01", // string
      "totalDistricts": 9, // number
      "districtsData": [ // Array<object>
        {
          "districtEngName": "CHANTHABOULY", // string
          "districtLaoName": "ຈັນ​ທະ​ບູ​ລີ", // string
          "districtCode": "0101", // string
          "totalVillages": 36, // number
          "villagesData": [ // Array<object>
            {
              "villageEngName": "NONGPING", // string
              "villageLaoName": "ໜອງປິງ", // string
              "villageCode": "0101001" // string
            },
            {
              "villageEngName": "BORNANGOUA", // string
              "villageLaoName": "ບໍ່ນາງົວ", // string
              "villageCode": "0101002" // string
            }
          ]
        }
      ]
    }
  ]
}
```

## License

This project is open source and available under the [MIT License](LICENSE).

## Contributing

Contributions are welcome! Please open an issue or submit a pull request for any improvements or additions.

## Contact

For any questions or inquiries, please contact [i.xaiyaloun@gmail.com](i.xaiyaloun@gmail.com).

