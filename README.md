Hero Section:

<img width="1905" height="915" alt="image" src="https://github.com/user-attachments/assets/ad61d226-5e37-431d-ba7b-bb6e2bbbc84e" />



Currently Available Movie:

<img width="1919" height="887" alt="image" src="https://github.com/user-attachments/assets/cde5ec87-bf6a-4c44-97a0-692827d9e4e7" />




Trailer Section:

<img width="1904" height="903" alt="image" src="https://github.com/user-attachments/assets/0b5716dc-063c-4ad1-8ccf-1937a86531ff" />



Footer:

<img width="1916" height="903" alt="image" src="https://github.com/user-attachments/assets/1c7d304c-d159-4701-8abc-ec0653b60d3d" />



All Movies:

<img width="1910" height="902" alt="image" src="https://github.com/user-attachments/assets/14e38991-1758-496d-9b98-b503a99846a0" />



Movie Details:

<img width="445" height="5084" alt="quick-show-client-updated vercel app_movies_911430" src="https://github.com/user-attachments/assets/e8a23960-1b94-4e73-86c9-a626a2f29dfe" />




Favorites:

<img width="1919" height="907" alt="image" src="https://github.com/user-attachments/assets/bce498ba-b74f-46cb-8e64-e5379141d82d" />


My Bookings:

<img width="1915" height="893" alt="image" src="https://github.com/user-attachments/assets/ffb47c79-1d7b-4aab-831d-b2f3e82133c4" />



Admin Dashboard:

<img width="1905" height="911" alt="image" src="https://github.com/user-attachments/assets/b6265706-f34b-47bf-a3eb-4eec3dfed6bc" />



Add Shows:

<img width="1919" height="898" alt="image" src="https://github.com/user-attachments/assets/5ef98876-15bb-4d23-8a5f-e28eb5d165bc" />



List of Shows:

<img width="1919" height="903" alt="image" src="https://github.com/user-attachments/assets/729e2afe-c7cc-4ad5-865c-ba4aeb35b31f" />


List of Bookings:

<img width="1919" height="894" alt="image" src="https://github.com/user-attachments/assets/426fa287-17a5-4235-8e41-0c0364914330" />






# QuickShow 🎬
A movie ticket booking platform with real-time seat selection and admin management.

## Features
- Browse and book movies
- Role-based user and admin dashboards
- Real-time seat selection
- Payment integration

## Tech Stack
React, Express, MongoDB, Clerk, Inngest, Tailwind CSS

## 📊 Data Flow Diagram (DFD) – QuickShow

```mermaid
flowchart TD

%% External Entities
User([User]):::ext
Admin([Admin]):::ext
Payment([Payment Gateway]):::ext

%% Processes
Auth{{Clerk Authentication}}
Booking{{Booking System}}
Seat{{Seat Management}}
PaymentP{{Payment Processing}}
AdminM{{Admin Management}}
Inngest{{Inngest Job Scheduler}}

%% Data Stores
DB[(MongoDB Database)]
Movies[(Movies Collection)]
Users[(Users Collection)]
Bookings[(Bookings Collection)]
Payments[(Payments Collection)]

%% Flows
User -->|Login/Register| Auth
Admin -->|Login| Auth
Auth --> Users

User -->|Browse Movies| Movies
User -->|Book Ticket| Booking
Booking --> Seat
Seat --> Bookings
Booking --> PaymentP
PaymentP --> Payment
Payment --> PaymentP
PaymentP --> Payments
Inngest --> Seat

Admin -->|Manage Movies/Shows| AdminM
AdminM --> Movies
AdminM --> Bookings
AdminM --> Payments

%% Styling
classDef ext fill=#f4a261,stroke=#333,stroke-width=2px;
classDef process fill=#2a9d8f,stroke=#fff,stroke-width=2px,color=white;
classDef store fill=#e9c46a,stroke=#333,stroke-width=2px;

class Auth,Booking,Seat,PaymentP,AdminM,Inngest process;
class DB,Movies,Users,Bookings,Payments store;


## Setup Instructions
```bash
git clone https://github.com/Suraj4896/QuickShow.git
cd QuickShow
npm install
npm start


