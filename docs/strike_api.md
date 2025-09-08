## strike api

https://app.strikefinance.org/api/staking/getAllStake

https://app.strikefinance.org/api/staking/feeWalletBalance

https://app.strikefinance.org/api/perpetuals/getPoolInfoV2

https://app.strikefinance.org/api/perpetuals/getPoolInfo

https://app.strikefinance.org/api/prices/snek

https://app.strikefinance.org/api/perpetuals/getSnekOverallInfo

https://app.strikefinance.org/api/analytics/fees

https://app.strikefinance.org/api/perpetuals/getOverallInfo









## minswap api

https://agg-api.minswap.org/aggregator/ada-price?currency=usd



https://docs.minswap.org/developer/aggregator-api

https://agg-api.minswap.org/aggregator/tokens
{query: "STRIKE", only_verified: true}



const response = await fetch('https://agg-api.minswap.org/aggregator/tokens', {
    method: 'POST',
    headers: {
      "Content-Type": "application/json"
    },
    body: JSON.stringify({
      "query": "min",
      "only_verified": true,
    })
});

const data = await response.json();
