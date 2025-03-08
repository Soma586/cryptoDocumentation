---
sidebar_position: 3
---

# State Management


## Why I chose React Query over  Zustand  and Context API


After some research React query turn out to be a better option for data fetching, caching, and synchronization.

Key Features:

- Automatic caching and background refetching.
- Built-in loading and error states.
- Deduplication of requests (avoids duplicate API calls).
- Optimistic updates and pagination support.
- Devtools for debugging.

Use Case: Ideal for managing server state (e.g., API data).


Zustand and the Context API are better suited for global state management and sharing data across components. However, for a simple single-page app like tracking cryptocurrency prices, they weren’t really necessary. That said, if we were to expand the app to handle features like user authentication or sharing data across different pages in a more robust website, Zustand or the Context API would become much more relevant and useful.