## Parking Lot Management System


This is a command line util tool to replicate a parking lot management system


I own a parking lot that can hold up to `n` cars at any given point in time. Each slot is given a number
starting at 1 increasing with increasing distance from the entry point in steps of one. 


I want to create an automated ticketing system that allows my customers to use my parking lot without human intervention.


When a car enters my parking lot, I want to have a ticket issued to the driver. The ticket issuing process
includes us documenting the registration number (number plate) and allocating
an available parking slot to the car before actually handing over a ticket to the driver (we assume that our
customers are nice enough to always park in the slots allocated to them). The customer should be
allocated a parking slot which is nearest to the entry. At the exit the customer returns the ticket with the
time the car was parked in the lot, which then marks the slot they were using as being available. Total
parking charge should be calculated as per the parking time. Charge applicable is **$10 for first 2 hours**
and **$10 for every additional hour**.


We interact with the system via a simple set of commands which produce a specific output. Please take a
look at the example below, which includes all the commands you need to support - they're self-
explanatory. The system should accept a filename as a parameter at the command prompt and read the
commands from that file.

---


### Installation

To install all dependencies, compile and run test:
```
$ bin/setup
```

To run the application from the cmd-line so that it accepts a file:
```
$ bin/parking_lot_file ;file_inputs.txt
```

---


### Commands
- Create a parking lot of size n: create_parking_lot $capacity
- Park a car: park $reg_num
- Unpark car: leave $reg_num $hours
- Get status of car at any given time: status


---


### Assumptions


Below are the assumptions made while desigining the application

- It is a single floor parking lot
- The parking spaces are of the same type (no special parking/bike parking/etc)
- It is a single entry-exit parking lot, hence removing any concurrent entry
- There is no waiting queue. In case of full, the next incoming car is said 'bye !'


