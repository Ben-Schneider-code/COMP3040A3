# **Manitoba Event Planner**

## **API Description**
This is a REST API that provides resources to help Manitobans plan their events. This API allows Manitobans to obtain information about the weather and the venue where they are holding their event.

## **Endpoints**

### **Weather**  
This endpoint represents the weather in Manitoban cities. 

**Parameters**
- **city** : the name of the city about which the user wants the weather information.  
- **unit** : the unit that the user wants their temperature value in.

**Example Query**  
`https://ManitobaEventPlanner.com/weather/?unit=celcius&city=winnipeg`

### **Venue**  
This is an endpoint that represents places for holding events in Manitoba.
  
**Parameters**
- **name** : the name of venue where the user is holding their event.  
- **time** : the time the event is being held at the venue.  

**Example Query**  
`https://ManitobaEventPlanner.com/venue/?name=zoo&time=1:00pm`

## Resources

**Weather Resource**  

This resource represents information about the weather.
```
{  
    "temperature": number,
    "precipitation": string,
    "cloud-coverage": string
}  
```

**Venue Resource**  

This resource represents the venue the event is being held at.
```
{
    "busy": boolean,
    "event-types": [string],
    "rating": number
}
```

## Samples
**Weather sample request and response**
```
Request: https://ManitobaEventPlanner.com/weather/?unit=celcius&city=winnipeg
Response: 
{  
    "temperature": -5,
    "precipitation": "snowy",
    "cloud-coverage": "cloudy"
}  
```
```
Request: https://ManitobaEventPlanner.com/weather/?unit=celcius&city=brandon
Response: 
{  
    "temperature": -1,
    "precipitation": "ice-pellets",
    "cloud-coverage": "clear sky"
}  
```

**Venue sample request and response**
```
Request: https://ManitobaEventPlanner.com/venue/?name="Copa Banquet Centre"&time=1:00pm
Response: 
{
    "busy": false,
    "event-types": ["Wedding parties", "Birthday parties"],
    "rating": 4.2
}
```
