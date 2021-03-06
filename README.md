# api-documentation

FORMAT: 1A
HOST: https://polls.apiblueprint.org/

# mahasiswa
Membuat API mahasiswa

## Mahasiswa [/mahasiswa{?order}]

### List All Mahasiswa [GET]

Untuk melihat semua Mahasiswa

+ Parameters
    
    + order : NIM (string, optional) - Sorting user by field

+ response 200 (aplication/json)
            
            {
            "status": "OK",
            "message": "Successful",
            "data": [
                {
                    "id" : 1,
                    "name": "Muhammad Iqbal",
                    "NIM": "15014198",
                    "created_at": "2020-03-11T07:21:52.754Z",
                    "updated_at": "2020-03-11T07:28:52.754Z",
                    "token": "AkasnASNF121anSKNfaknfa"
                }, 
                {
                    "id" : 2,
                    "name": "Ilham Saputra",
                    "NIM": "1239817",
                    "created_at": "2020-03-11T07:21:52.754Z",
                    "updated_at": "2020-03-11T07:28:52.754Z",
                    "token": "AkasnASNF121anSKNfaknfa"
                }, 
                {
                    "id" : 3,
                    "name": "Aziz",
                    "NIM": "8732648723",
                    "created_at": "2020-03-11T07:21:52.754Z",
                    "updated_at": "2020-03-11T07:28:52.754Z",
                    "token": "AkasnASNF121anSKNfaknfa"
                }
            ]
        }
        
### Create a new Mahasiswa [POST]

Untuk membuat data mahasiswa baru. 

+ Request (application/json)

        {
            "name": "Dodik Prasetyo",
            "NIM": "12312343"
        }

+ Response 201 (application/json)

    + Body

            {
                "status": "OK",
                "message": "Successful",
                "data": {
                    "id" : 4,
                    "name": "Dodik Prasetyo",
                    "NIM": "12312343",
                    "created_at": "2020-03-11T07:28:52.754Z",
                    "updated_at": "",
                    "token": "AkasnASNF121anSKNfaknfa"
                }
            }
            
## Mahasiswa Collection with path [/mahasiswa/{id}]

### Update of Mahasiswa [PATCH]
Mengubah sebagian data mahasiswa

+ Parameters

    + id : 1 (number, required) - An unique identifier of the message

+ Response 200 (application/json)

    + Body
    
            {
                "status": "OK",
                "message": "Successful",
                "data": {
                    "id" : 1,
                    "name": "Muhammad Iqbal Ramadhan"
                }
            }
            
### Delete of Mahasiswa [DELETE]
Menghapus data mahasiswa

+ Parameters
    
    + id: 1 (number, required) 

+ Response 204 (application/json)

### Update all of Mahasiswa [PUT]
Mengubah data mahasiswa (keseluruhan)

+ Parameters

    + id : 1 (number, required) - An unique identifier of the message

+ Response 200 (application/json)

    + Body
    
            {
                "status": "OK",
                "message": "Successful",
                "data": {
                    "id" : 1,
                    "name": "M. Iqbal Rahamadahn",
                    "NIM": "150141997",
                    "created_at": "2020-03-11T07:21:52.754Z",
                    "updated_at": "2020-03-12T07:33:52.754Z",
                    "token": "AkasnASNF121anSKNfaknfa"
                }
            }
        
