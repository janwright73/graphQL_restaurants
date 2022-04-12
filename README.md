# graphQL_restaurants

Exercise uses restaurant data in
restaurants.json to perform CRUD actions using graphQL

# GraphQL

## here are the query and mutation structures

query getrestaurant($iid: Int =1) {
  restaurant(id:$iid){
    name 
    description
  }
}

query getrestaurants{restaurants {
  name
  description
  dishes {
    name
    price
  }
}}

mutation setrestaurant{
  setrestaurant(input: {
    name: "Granite",
    description: "American"}){
    name
    description
  }
}

mutation deleterestaurant($iid:Int =3){
  deleterestaurant(id: $iid){
    ok
  }
}

mutation editrestaurant($iid: Int = 0, $name: String = "fool"){
  editrestaurant(id: $iid, name: $name){
    description
  }
}