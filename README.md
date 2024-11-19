# Booking Microservices API  

This project is a **Booking Microservices API** built in C# using **.NET Core**.

## The goals of this project 
- Use layered architecture and repository pattern to build 5 microservices.
- Use Ocelot to build API gateway, which acts as a single entry point for external clients, routing requests to appropriate services and providing authentication.  
- Use Rabbitmq on top of Masstransit for Event Driven Architecture between our microservices.
- Use MSSql to create databases for each microservice.  
- Use docker to containerize each microservice.
- Use Nunit to write unit tests.
---

## The Domain And Bounded Context 
1. **Flight Service** is a bounded context CRUD service to handle flight related operations.<br/>
   **Key operations**: Check availability, reserve flight, release flight.
2. **Passenger Service** is a bounded context for managing passenger information.<br/>
   **Key operations**: Create passenger, update passenger, delete passenger.
3. **Booking Service** is a bounded context for managing all operation related to booking ticket.<br/>
   **Key Operations**: Create booking, update booking, cancel booking.
4. **Payment Service** is a bounded context for managing payment operations.<br/>
   **Key Operations**: Initiate payment, confirm payment, process refund.
5. **Notification Service** is a bounded context for sending notifications to users for booking confirmations, cancellations, reminders, and updates.<br/>
    **Key Operations**: Consume events and send emails.
![diagram-export-11-19-2024-7_43_12-PM](https://github.com/user-attachments/assets/a0399419-0ef4-409e-a137-685df556abfc)
