-User
user_id (PK)
first_name, last_name, email, password_hash, phone_number, role, created_at

-Property
property_id (PK)
host_id (FK → User)
name, description, location, pricepernight, created_at, updated_at

-Booking
booking_id (PK)
property_id (FK → Property)
user_id (FK → User)
start_date, end_date, total_price, status, created_at

-Payment
payment_id (PK)
booking_id (FK → Booking)
amount, payment_date, payment_method

-Review
review_id (PK)
property_id (FK → Property)
user_id (FK → User)
rating, comment, created_at

-Message
message_id (PK)
sender_id, recipient_id (FKs → User)
message_body, sent_at

+Define the Relationships:
User – Property: One user (host) can have many properties.

User – Booking: One user (guest) can make many bookings.

Property – Booking: One property can have many bookings.

Booking – Payment: One booking can have one payment.

User – Review – Property: A user can write many reviews for properties.
