# Cleaner

This worker is responsible for cleaning up the server. It will delete files after a certain amount of time.

## Test Cron Triggers using Wrangler

```sh
npx wrangler dev --test-scheduled
curl "http://localhost:8787/__scheduled?cron=0+*+*+*+*"
```
source: https://developers.cloudflare.com/workers/examples/cron-trigger/#test-cron-triggers-using-wrangler
