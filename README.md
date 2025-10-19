# 🅿️ Parking Lot System Design

A comprehensive object-oriented parking lot system implementation demonstrating various design patterns and software engineering principles.

## 🚀 Features

- **Multiple Vehicle Types**: Car, Truck, Electric, Van, Motorbike
- **Smart Parking Allocation**: Type-based spot assignment
- **Multiple Payment Methods**: Cash, Credit Card, etc.
- **Real-time Display Updates**: Observer pattern for live spot availability
- **Design Patterns**: Singleton, Factory, Strategy, Observer, Command, Template Method

## 🏗️ Design Patterns Used

| Pattern | Implementation | Purpose |
|---------|----------------|---------|
| Singleton | `ParkingLot` | Single instance management |
| Factory Method | `VehicleFactory`, `ParkingSpotFactory` | Object creation |
| Strategy | `PaymentStrategy` | Flexible payment processing |
| Observer | `ParkingDisplayBoard` | Real-time updates |
| Command | `ProcessTicketCommand` | Decoupled ticket processing |
| Template Method | `ParkingSpot` | Consistent parking behavior |

## 🛠️ Quick Start

```java
// Get parking lot instance (Singleton)
ParkingLot parkingLot = ParkingLot.getInstance();

// Create vehicle (Factory Method)
VehicleFactory carFactory = new CarFactory();
Vehicle car = carFactory.createVehicle();

// Get parking ticket
ParkingTicket ticket = parkingLot.getNewParkingTicket(car);

// Process payment (Strategy Pattern)
PaymentStrategy payment = new CashPaymentStrategy();
payment.pay(ticket);
