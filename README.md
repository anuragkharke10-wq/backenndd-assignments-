Backend Assignments

This repository contains all the assignments for the Node.js Backend subject — core JavaScript exercises, native HTTP servers, file handling, DOM event handling, and a full Express.js REST API.

All basic assignments run on plain Node.js with no external packages (only the built-in http, fs, and path modules). Only Major Assignment 3 requires installing Express.

Basic Assignments
Assignment 1 — Shopping Cart System

Calculate the final price of items added to a cart. For each item, subtract a discount from the price, apply a fixed 10% tax on the discounted amount, and add it to a running cart total. Prints each item's final price and the overall cart value.

Run: node assignment1.js

Assignment 2 — User Profile Management

Demonstrate JavaScript data types by building a user profile using primitive types (string, number, boolean, null, symbol) and non-primitive types (object, array). Includes a function that returns a greeting and logs a nested object property, an array element, and the greeting.

Run: node assignment2.js

Assignment 3 — Library Management System

A library object that manages books — add a book, borrow a book (mark unavailable), return a book (mark available), and display all books with their availability. Handles edge cases like borrowing an already-borrowed book or an unknown ISBN.

Run: node assignment3.js

Assignment 4 — Multiplication Table

A function that takes a number and prints its multiplication table from 1 to 10 using a for loop.

Run: node assignment4.js

Assignment 5 — ATM Withdrawal Simulation

Simulate an ATM. Given a starting balance and a fixed withdrawal amount, keep withdrawing using a while loop until the balance is insufficient, then stop using break. Prints each transaction and the final balance.

Run: node assignment5.js

Assignment 6 — Find the First Even Number

A function that finds the first even number in an array using a do-while loop and the continue statement to skip odd numbers. Handles empty arrays and arrays with no even numbers.

Run: node assignment6.js

Assignment 7 — Print Day of the Week

Get the current day using the Date object and print its name ("Monday", etc.) using a switch statement.

Run: node assignment7.js

Assignment 8 — College Grading System

A function that takes a score and returns a letter grade (A/B/C/D/F) based on ranges, using if-else conditions.

Run: node assignment8.js

Assignment 9 — Validate JSON Payload with a Custom Module

A native Node.js HTTP server that accepts POST requests with a JSON body and validates the payload using a separate custom module (validateUser.js). Returns 200 for a valid user, and 400 with an error message for invalid JSON or failed validation.

Run: node assignment9.js (server on http://localhost:3000 — stop with Ctrl+C)

Test:

bash
curl -X POST http://localhost:3000 -H "Content-Type: application/json" \
  -d '{"name":"Anurag","email":"anurag@test.com","age":21}'
Assignment 10 — RTO Vehicle Registration (File Persistence)

Registers student vehicles and saves records to rto_data.json using the fs module. Each entry stores name, college ID, vehicle number, type, and an auto-generated registration date. Appends to the file if it already exists.

Run: node assignment10.js

Assignment 11 — Student Registration Server

A native HTTP server (no Express) that accepts POST requests to register a student, adds a registeredAt timestamp, and appends each student to students.json. Returns 201 on success, 400 for invalid JSON.

Run: node assignment11.js (server on http://localhost:4000 — stop with Ctrl+C)

Test:

bash
curl -X POST http://localhost:4000 -H "Content-Type: application/json" \
  -d '{"studentName":"Anurag","course":"BTech CSE"}'
Major Assignments
Major Assignment 1 — RailConnect Live Ops Dashboard

major-assignment-1/

Given a dataset of train booking records (Train 12951 - Mumbai Rajdhani Express), build an operations dashboard using only fat-arrow functions and array methods — no for or while loops. Produces:

Occupancy summary — confirmed / waitlisted / RAC counts and occupancy rate
Revenue breakdown — total revenue, broken down by coach class and booking status
Station load — passengers boarding from each station
Vulnerable passengers — confirmed passengers under 12 or 60+
Waitlist clearance plan — waitlisted passengers ranked by PNR

All combined into one dashboard object and printed with console.log().

Run: node major-assignment-1/opsDashboard.js

Major Assignment 2 — Interactive E-Commerce Product Card

major-assignment-2/

A product card web page that attaches DOM event listeners using addEventListener():

Click — open product details, demonstrating the difference between event.target and event.currentTarget
Double-click — zoom the product image
Mouseover / mouseout — change and restore the card border
Add to Cart / Wishlist / Delete buttons — using event.stopPropagation(), event.preventDefault(), and a confirmation dialog before removing the card from the DOM
