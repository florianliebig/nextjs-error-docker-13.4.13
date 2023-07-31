# Steps to reproduce

```sh
docker build -t next-test --no-cache . && docker run -p 3000:3000 --env API_BASE=https://www.google.com --name next-test next-test
```

Visit any page, check for API_BASE in Node terminal. process.env is console.logged in middleware.ts. API_BASE will not be available in process.env

Downgrade next in package.json to 13.4.12. Run npm i and rerun the commands above. API_BASE will be available.