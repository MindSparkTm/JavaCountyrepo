
Architecture of the API
Version -v.0

The architecture is a three tier model.
1. The Controller.
2. The Service Layer
3. The Data Layer


So, when a request comes at the url(/county?data=Nairobi)
it goes to the getallinfo method
1. The getallmethod calls the service (DataService)
2. The dataservice does all the file reading and fills up the model
with county, subcounty and ward values.
3. The controller calls the model to do appropriate parsing.
4. After all the parsing is done, the data is now added to the jsonobject  class
5. The jsonobject is then converted to jsonstring and returned as json

http://localhost:8080/county?data=Nairobi

response
{
    "info": {
        "response": "success",
        "county": "Nairobi",
        "subcounty": [
            "Westlands",
            "Dagoreti North",
            "Dagoretti South",
            "Langata",
            "Kibera",
            "Roysambu",
            "Kasarani",
            "Ruaraka",
            "Embakasi South",
            "Embakasi North",
            "Embakasi Central",
            "Embakasi East",
            "Embakasi West",
            "Makadara",
            "Kamukunji",
            "Starehe",
            "Mathare"
        ],
        "wards": [
            [
                "Kitisuru",
                "Parklands/ Highridge",
                "Karura",
                "Kangemi",
                "Mountain View"
            ],
            [
                "Kilimani",
                "Kawangware",
                "Gatina",
                "Kileleshwa",
                "Kabiro"
            ],
            [
                "Mutu-ini",
                "Ngando",
                "Riruta",
                "Uthiru/ Ruthimitu",
                "Waithaka"
            ],
            [
                "Karen",
                "Nairobi West",
                "Mugumo-ini",
                "South C",
                "Nyayo Highrise"
            ],
            [
                "Laini Saba",
                "Lindi",
                "Makina",
                "Woodley/ Kenyatta Golf Course",
                "Sarang'ombe"
            ],
            [
                "Githurai",
                "Kahawa West",
                "Zimmerman",
                "Roysambu",
                "Kahawa"
            ],
            [
                "Clay City",
                "Mwiki",
                "Kasarani",
                "Njiru",
                "Ruai"
            ],
            [
                "Babadogo",
                "Utalii",
                "Mathare North",
                "Lucky Summer",
                "Korogocho"
            ],
            [
                "Imara Daima",
                "Kwa Njenga",
                "Kwa Reuben",
                "Pipeline",
                "Kware"
            ],
            [
                "Kariobangi North",
                "Dandora Area I",
                "Dandora Area II",
                "Dandora Area III",
                "Dandora Area IV"
            ],
            [
                "Kayole North",
                "Kayole Central",
                "Kayole South",
                "Komarock",
                "Matopeni/ Spring Valley"
            ],
            [
                "Upper Savanna",
                "Lower Savanna",
                "Embakasi",
                "Utawala",
                "Mihango"
            ],
            [
                "Umoja I",
                "Umoja II",
                "Mowlem",
                "Kariobangi South"
            ],
            [
                "Maringo/Hamza",
                "Viwandani",
                "Harambee",
                "Makongeni"
            ],
            [
                "Pumwani",
                "Eastleigh North",
                "Eastleigh South",
                "Airbase",
                "California"
            ],
            [
                "Nairobi Central",
                "Ngara",
                "Pangani",
                "Ziwani/Kariokor",
                "Landimawe",
                "Nairobi South"
            ],
            [
                "Hospital",
                "Mabatini",
                "Huruma",
                "Ngei",
                "Mlango Kubwa",
                "Kiamaiko"
            ]
        ]
    }
}