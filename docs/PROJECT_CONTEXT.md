# Restaurant Menu & Management System — Project Context

## Purpose
Build two distinct experiences:
1. A public-facing digital menu for customers.
2. A private management interface for restaurant staff.

Keep the customer experience mobile-friendly and the management workflows clear and efficient.

## Primary users
Customers browsing the menu; restaurant owners or managers maintaining menu content; staff handling orders if order management is included.

## Core workflows to explore
1. Browse menu categories and items.
2. View item descriptions, prices, and availability.
3. Maintain categories and menu items in the admin area.
4. Mark menu items available or unavailable.
5. Create and track orders, if included in the MVP.
6. Associate orders with tables, if table management is included.

## MVP candidates
Public menu; menu category and item management; item price, description, image and availability; protected admin interface; basic order workflow; table management; simple daily activity dashboard. The project owner decides which belong in the first release.

## Product decisions to resolve
- Single restaurant or multiple restaurants
- Browse-only menu or customer ordering
- Whether QR codes are needed in the first release
- Dine-in, takeaway, or both
- Order states and who can change them
- Whether table management is required
- Whether taxes, discounts, modifiers, or add-ons are in scope
- Image storage and management
- Whether kitchen display or printing is needed

## Security and operational constraints
- Protect admin and staff routes.
- Public menu access must not expose management functions.
- Validate order and menu data on the server where applicable.
- Do not store payment card data. Payment integration is out of scope unless explicitly approved and implemented through a suitable provider.
- Use demo data only; never commit real customer or restaurant data.

## Technical status
No framework, database, authentication approach, or deployment platform is prescribed yet. Inspect the repository and agree on architecture before generating the application.

## AI agent guidance
- Inspect the repository and this document before proposing changes.
- Ask the project owner to resolve important product and architecture decisions; do not invent business rules.
- Use relevant skills already installed in the agent environment. Do not duplicate skill definitions in the repository.
- Document setup, environment variables, and verification commands once chosen.
- Never commit secrets or real business/customer data.
- Never claim a feature is implemented or tested unless verified.

**Project status:** Initial repository setup. Update this as milestones are completed.
