# HotelBooking OOP

This project is a Python-based hotel booking system that reads hotel availability and customer credit card information from CSV files. It allows users to book a hotel if available, after validating their credit card and authenticating the payment. The system generates a reservation confirmation upon successful booking.
Features

    Hotel Availability Check: Users can select a hotel to book based on its availability.
    Credit Card Validation: Validates the provided credit card details (number, expiration, holder, and CVC) with a record in a CSV file.
    Secure Credit Card Authentication: Adds an extra layer of security by authenticating the credit card with a password.
    Reservation Confirmation: Generates a reservation receipt upon successful booking.

Prerequisites

Make sure you have Python installed and the following packages:

    Pandas: Used for reading and manipulating CSV files.

Install Pandas using pip if you haven't already:

bash

pip install pandas

CSV Files

The system reads data from three CSV files:

    hotels.csv: Contains hotel details such as id, name, and availability.
    cards.csv: Contains valid credit card data, including number, expiration, holder, and cvc.
    card_security.csv: Contains credit card numbers and their corresponding passwords for authentication.

Sample structure for these files:

    hotels.csv

    csv

id,name,available
1,Hotel A,yes
2,Hotel B,no
3,Hotel C,yes

cards.csv

csv

number,expiration,holder,cvc
1234567890123456,12/26,JOHN SMITH,123
9876543210987654,11/25,JANE DOE,456

card_security.csv

csv

    number,password
    1234567890123456,mypass
    9876543210987654,password123

How It Works

    Hotel Availability: The system first checks if the hotel selected by the user is available for booking by reading the hotels.csv file.
    Credit Card Validation: After the hotel is selected, the user’s credit card details are validated against the cards.csv file to ensure the card information is correct.
    Authentication: For added security, the credit card password is verified using the card_security.csv file.
    Booking Confirmation: If all steps are successful, the hotel booking is confirmed, and a reservation ticket is generated for the user.

Running the Program

    Clone or download the project.
    Ensure the required CSV files (hotels.csv, cards.csv, card_security.csv) are available in the same directory as the script.
    Run the Python script:

bash

python hotel_booking.py

    Follow the prompts to enter the hotel ID, your name, and the credit card details.

Example Usage

yaml

   id    name available
0   1  Hotel A       yes
1   2  Hotel B        no
2   3  Hotel C       yes
Enter the ID of the hotel: 1
Enter your name: John Doe
Thank you for your reservation!
Here are you booking data:
Name: John Doe
Hotel name: Hotel A

Project Structure

bash

project-folder/
│
├── hotels.csv            # Hotel data (availability, names)
├── cards.csv             # Credit card details (for validation)
├── card_security.csv     # Credit card passwords (for authentication)
├── hotel_booking.py      # Main Python script
└── README.md             # This readme file

Notes

    Ensure that the hotel and credit card information in the CSV files is accurate.
    The system is designed to run locally and is not production-ready. You may need to customize it for more complex real-world scenarios.
