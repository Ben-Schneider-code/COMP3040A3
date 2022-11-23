# **Manitoba Event Planner**

## **API Description**
This is an REST API that provides resource to help Manitobians plan their events. This API allows Manitobians to obtain information about the weather and destination they are holding their event.  

## **Endpoints**

### **Weather**  
This is an endpoint represents weather in Manitobian cities.  

**Parameters**
- **city** : the name of the city the user wants weather information about  
- **unit** : the unit that the user wants their temperature value in  

**Example Query**
`https://ManitobaEventPlanner/weather/?unit=celcius&city=winnipeg`

### **Venue**  
This is an endpoint that represents places for holding events in Manitoba.
  
**Parameters**
- **name** : the name of venue where the user is holding their event.  
- **time** : the time the event is being held at the venue.  
**Example Query**
https://ManitobaEventPlanner/venue/?name=zoo?time=1:00pm

## Resources

**Weather Resource**  

This resource represents information about the weather.
```
{  

    "temperature": number  
    "precipation": string
    "cloud-coverage": string
}  
```

**Venue Resource**  

This resource represents the venue the event is being held at.
```
{
    "busy": boolean
    "event-types": [string]  
    rating: number
}
```  
