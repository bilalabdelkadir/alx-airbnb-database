# Database Normalization - 3NF

## Overview

In this task, I made sure my database follows **Third Normal Form (3NF)** to remove extra data and keep it organized. First, I made the database follow **First Normal Form (1NF)** and **Second Normal Form (2NF)**. Then, I worked on removing unnecessary data connections to reach **3NF**.

## Normalization Steps

1. **1NF**:

   - Each column has only one value, and each record is unique.

2. **2NF**:

   - All information in the table depends on the main key. There is no information that only depends on part of the key.

3. **3NF**:
   - I removed any unnecessary connections between the data. For example, I moved the `BookingStatus` and `PaymentMethod` to their own tables so I don't store them in many places.

## Changes Made

- I moved the **PaymentMethod** and **BookingStatus** into separate tables to avoid storing the same information again and again.
- I added **foreign keys** to make sure the tables are connected properly.

## Conclusion

By using these normalization steps, the database is now easier to manage, faster to use, and keeps data organized without repetition.
