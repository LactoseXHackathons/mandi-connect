# Mandi Link

Build "Mandi Connect" — a live market price & direct farmer-buyer platform for Indian agriculture. Use React + Tailwind with Supabase for auth and database.

CORE PURPOSE:

Farmers compare live mandi (market) prices across locations to decide where to sell, list their produce directly, and connect with buyers without middlemen. Buyers browse/search farmer listings and connect directly.

DESIGN STYLE:

Clean, warm, agriculture-themed UI — earthy green (#2D6A4F) and warm orange/amber (#E76F00) accents on a soft off-white background. Large, high-contrast text and big tap targets (this app is used by farmers and buyers, many on basic smartphones with low digital literacy). Icons paired with plain-language text labels (never icon-only). Rounded cards, generous spacing, mobile-first responsive layout. Include a simple English/Hindi language toggle in the header.

USER ROLES:

On first login, ask "I am a Farmer" or "I am a Buyer" and route to a role-specific home screen. Simple phone-number based login (mock OTP is fine for demo).

SUPABASE TABLES:

1. users: id, name, phone, role (farmer/buyer), location

2. mandi_prices: id, crop_name, mandi_name, location, price_per_quintal, updated_at

3. listings: id, farmer_id, crop_name, quantity, expected_price, location, photo_url, status (available/sold), created_at

Seed mandi_prices with sample data for 4-5 crops (Wheat, Rice, Onion, Tomato, Cotton) across 4-5 mandi locations with varying prices, so the price comparison feature works out of the box.

PAGES/SCREENS:

1. Landing/Login: App name "Mandi Connect", tagline "Sell Smart. Sell Direct.", role selection, phone login.

2. Farmer Home Dashboard:

   - "Best Prices Near You" — top 3 crop/mandi price cards

   - Quick action button "Sell My Crop" (large, prominent)

   - "My Listings" section showing their active listings with status badges (Available/Sold)

3. Live Price Board (Farmer view):

   - Filterable by crop and location

   - Card/table showing: Crop, Mandi Name, Location, Price per Quintal, Last Updated

   - Sort by "Best Price" button

   - Highlight the highest price for the selected crop

4. Sell My Crop (Farmer form):

   - Simple form: Crop (dropdown with icons), Quantity, Expected Price, Location, Contact Number, optional Photo upload, Available From date

   - Big "List My Produce" submit button

   - Confirmation screen after submit

5. Buyer Home Dashboard:

   - Prominent search bar ("Search crops, e.g. Wheat, Onion")

   - Browse listings grid (crop photo/icon, crop name, quantity, price, location, farmer name)

   - Filter by crop type, location, price range

6. Listing Detail Page:

   - Full listing info, farmer name and location

   - Large "Connect with Farmer" button that reveals phone number and offers a WhatsApp link

   - "Back to search" navigation

7. My Listings (Farmer) / Saved Listings (Buyer): simple list view with edit/delete (farmer) or unsave (buyer)

KEY UX RULES:

- Every core action (list produce, find best price, connect with a farmer) should take 3 taps or fewer

- Always show currency as ₹ and unit as quintal

- Use plain language button labels, not technical terms ("Sell My Crop" not "Create Listing", "Connect" not "Initiate Contact")

- Mobile-first: design for a single-column layout that works well on small screens first, then scale up

Build this as a working prototype with the seeded data, functioning navigation between all screens, and working forms that write to Supabase.

This project was built with [Lovable](https://lovable.dev).

## Build with Lovable

Continue developing this project in the [Lovable editor](https://lovable.dev/projects/078667b0-8dfd-4b04-bf65-fc69a831b6e0).

- **Ship faster**: describe what you want to build and Lovable handles the code.
- **Stay in sync**: every change made in Lovable is committed straight to this repository.
- **Full ownership**: this code is yours. Push to `main` on GitHub and your changes sync back into Lovable, ready for your next prompt.

## Development

Prefer working locally? You need Node.js and npm — [install with nvm](https://github.com/nvm-sh/nvm#installing-and-updating).

```sh
git clone <this-repository-url>
cd <repository-name>
npm i
npm run dev
```
