We need to be able to target all the running instances of certain service, in order for them to update.

Containers do not know their environment.

# SNS subscription
- Obtain the ipaddress information of myself and create a subscription to a SNS 
- On terminate, unsubscribe to SNS
- Application is in charged to send the SNS message

### Advantages
- No extra API Service needed.

### Disadvantages
- Code duplication if more services need it.
- Authorization???


# Push Services API 

- Load all services from ECS Cluster
- Pushes notifications to all running instaces of a certain service.
- Control if a push notification has been carried out.

### Advantages
- The code that needs it only create the endpoint.
- Can have Status when notification is succesfully delivered.
- Extendable to other applications.

### Disadvantages
- Developing time
- Resources for API

![Push_notification_service.png](/.attachments/Push_notification_service-dc3f52e1-0141-43e0-aaea-5c8561b508e8.png)