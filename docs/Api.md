---
sidebar_position: 2
---

# API integration details

## How is data is fetched and updated


```js
const { data, isLoading, error, refetch, isRefetching } = useQuery({
      queryKey: ["cryptoData"],
      queryFn: async () => {
        const response = await fetch(
          "https://api.coingecko.com/api/v3/coins/markets?vs_currency=usd&order=market_cap_desc&per_page=100&page=1&sparkline=false&price_change_percentage=24h",
        )
        if (!response.ok) {
          throw new Error("Network response was not ok")
        }
        return response.json() 
      },
      staleTime: 60000, // 1 minute
    })
```

We are using the useQuery hook from React Query to fetch data from the CoinGecko API for the latest cryptocurrency price data.

We provided a queryKey that React Query uses to cache and manage the retrieved data.

The queryFn takes in a fetch function that retrieves the data and parses it into a JSON object.

The staleTime property ensures that the data is considered fresh for 1 minute before it becomes stale and needs to be refetched.