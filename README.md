# Simple Blockchain

This simple blockchain was made following Coral Health's [post on Medium](https://medium.com/@mycoralhealth/code-your-own-blockchain-in-less-than-200-lines-of-go-e296282bcffc).
It has educational purposes only.

## Getting started

Run
```bash
git clone https://github.com/gpressutto5/blockchain.git
cd blockchain
cp .env.example .env

go get github.com/davecgh/go-spew/spew
go get github.com/gorilla/mux
go get github.com/joho/godotenv

go run main.go
```

You can change the listening port on `.env`. The default port is 80.

You can add new blocks to the chain by sending a POST with a JSON, like this:

```bash
curl -H "Content-Type: application/json" -X POST -d '{"Value":50}' http://localhost
```

You can view the whole blockchain by accessing your localhost or sending a GET request, like this:

```bash
curl http://localhost
```
