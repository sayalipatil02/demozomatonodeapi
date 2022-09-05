page 1
> List of City
>> (Get)  http://localhost:9100/location
> List of Restaurant
>> (Get)  http://localhost:9100/restaurants
> Restaurant on the basis of city
>> (Get)  http://localhost:9100/restaurants?stateId=2
> List of QuickSearch
>> (Get)  http://localhost:9100/mealType


// page 2
> Restaurant on the basis of meal
>> (Get)  http://localhost:9100/restaurants?mealId=1
>>        http://localhost:9100/restaurants?stateId=2&&mealId=1
> Filter on basis of cuisine
>> (Get)  http://localhost:9100/filter/1?cuisineId=1
> Filter on basis of cost
>> (Get)  http://localhost:9100/filter/1?lcost=150&hcost=300
> Sort on basis of cost
>> (Get)  http://localhost:9100/filter/1?lcost=150&hcost=300&sort=-1


// page 3
> Details of the Restaurant
>> (Get)  http://localhost:9100/details/1  
> Menu of the Restaurant
>> (Get)  http://localhost:9100/menu/6


// page 4
> Menu details (selected item)
>>(Post)  localhost:9100/menuItem
> place order
>>(post)  localhost:9100/placeOrder
(
    {
        "name": "nikita",
        "email": "nikita@gmail.com",
        "add": "nasik main",
        "phone": 987453611520,
        "cost": 600,
        "menuItem": [1,2]
    }
)

// page 5
> List of order placed
>>(Get)  http://localhost:9100/orders
> List of order placed of particular user
>>(Get)  http://localhost:9100/orders?email=sayali@gmail.com
> Update order status
>>(put)  http://localhost:9100/updateOrder/2
(
    {
        "status":"Tax_fai",
        "bank_name":"AXIS",
        "date":"29/05/2023"
    }
)


///////////////////////////
> Delete order
>>(delete)  localhost:9100/deleteOrder/6315cee1db15978f244b5639