# Province, District and Village Data in Laos PDR (ຂໍ້ມູນແຂວງ, ເມືອງ ແລະ ບ້ານ ໃນປະເທດລາວ)
ໃນ Repo ນີ້ປະກອບມີໄຟລ json ທີ່ເກັບກໍາຂອງມູນ ແຂວງ, ເມຶອງ ແລະ ບ້ານ. ຂໍ້ມູນຖືກຈັດຮຽງໃນຮູບແບບ JSON ແລະ ປະກອບດ້ວຍຂໍ້ມູນເຊັ່ນ: ຊື່ເມືອງໃນພາສາອັງກິດ ແລະ ພາສາລາວ, ລະຫັດເມືອງ, ຊື່ບ້ານ ແລະຊື່ແຂວງ.

This project contains data for villages and districts in various provinces in Laos PDR. The data is structured in JSON format and includes information such as village names in both English and Lao, village codes, district names, and province names.

## Data Structure ໂຄງສ້າງຂໍ້ມູນ

ຂໍ້ມູນຖືກຈັດຮຽງໃນຮູບແບບ:
- **provinceEngName**: ຊື່ແຂວງພາສາອັງກິດ.
- **provinceLaoName**: ຊື່ແຂວງພາສາລາວ.
- **provinceCode**: ລະຫັດແຂວງ.
- **totalDistricts**: ຈຳນວນເມືອງທັງໝົດໃນແຂວງ.
- **districtsData**: ອາເມືອງຂອງເມືອງ, ທີ່ປະກອບດ້ວຍ:
    - **districtEngName**: ຊື່ເມືອງພາສາອັງກິດ.
    - **districtLaoName**: ຊື່ເມືອງພາສາລາວ.
    - **districtCode**: ລະຫັດເມືອງ.
    - **totalVillages**: ຈຳນວນບ້ານທັງໝົດໃນເມືອງ.
    - **villagesData**: ອາເມືອງຂອງບ້ານ, ທີ່ປະກອບດ້ວຍ:
        - **villageEngName**: ຊື່ບ້ານພາສາອັງກິດ.
        - **villageLaoName**: ຊື່ບ້ານພາສາລາວ.
        - **villageCode**: ລະຫັດບ້ານ.


The JSON data is organized as follows:
- **provinceEngName**: The name of the province in English.
- **provinceLaoName**: The name of the province in Lao.
- **provinceCode**: The code of the province.
- **totalDistricts**: The total number of districts in the province.
- **districtsData**: An array of district objects, each containing:
  - **districtEngName**: The name of the district in English.
  - **districtLaoName**: The name of the district in Lao.
  - **districtCode**: The code of the district.
  - **totalVillages**: The total number of villages in the district.
  - **villagesData**: An array of village objects, each containing:
    - **villageEngName**: The name of the village in English.
    - **villageLaoName**: The name of the village in Lao.
    - **villageCode**: The code of the village.

## Example

Here is an example of the data structure:

```json
{
  "provinceEngName": "ATTAPEU PROVINCE",
  "provinceLaoName": "ຂ. ອັດຕະປື",
  "provinceCode": "17",
  "totalDistricts": 5,
  "districtsData": [
    {
      "districtEngName": "SAMAKHIXAY DISTRICT",
      "districtLaoName": "ມ. ສະມາຄີໄຊ",
      "districtCode": "1701",
      "totalVillages": 48,
      "villagesData": [
        {
          "villageEngName": "PHONESAVUNG VILLAGE",
          "villageLaoName": "ບ. ໂພນສະຫວ່າງ",
          "villageCode": "1702020"
        },
        ...
      ]
    },
    ...
  ]
}
```

## Usage

You can use this data for various purposes such as:
- Geographic information systems (GIS)
- Data analysis and visualization
- Research and educational purposes

## License

This project is open source and available under the [MIT License](LICENSE).

## Contributing

Contributions are welcome! Please open an issue or submit a pull request for any improvements or additions.

## Contact

For any questions or inquiries, please contact [i.xaiyaloun@gmail.com](i.xaiyaloun@gmail.com).

