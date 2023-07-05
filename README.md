Instructions

Welcome to Lee's Central Massachusetts Car dealership repo. 

This API stores records for some of the biggest commercial car dealerships in Central MA.

With this API you can retrieve the name, address, or phone number of the dealership! You can even see if the dealership provides auto repair services so you can get specialized service for the make of your vehicle!

The API supports the following routes : GET all dealerships, GET a particular dealership, and, if I missed one, you can POST the information for a new dealership.

To get ALL dealerships send the following request through your browser : 

**GET** `http://localhost:1337/dealerships`

**Response**
```JSON
[{
  id: 1
  name: 'Acura Auburn',
  Address: '476 Sotuhbridge St Auburn MA 01501',
  phone: '5088320444',
  repairs: 'yes'
},
... all other dealerships
]
```


**GET** `http://localhost:1337/dealerships/1`

**Response**
```JSON
[{
  id: 1
  name: 'Acura Auburn',
  Address: '476 Sotuhbridge St Auburn MA 01501',
  phone: '5088320444',
  repairs: 'yes'
},
]

#### Create New Dealership

**POST** `http://localhost:1337/dealerships`

**Body**
```JSON
{
  name: 'Lees McLarens',
  Address: '100 Pirates Way Rt 146 Worcester MA 01505',
  phone: '5085555555',
  repairs: 'yes'
}
```

**Response**
```JSON
{
  id: 21,
  name: 'Lees McLarens',
  Address: '100 Pirates Way Rt 146 Worcester MA 01505',
  phone: '5085555555',
  repairs: 'yes'
  updatedAt: '2020-04-24T13:12:15.656Z',
  createdAt: '2020-04-24T13:12:15.656Z'
}
```