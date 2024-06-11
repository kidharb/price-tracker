1. Create a namespace called `pricetracker`

kubectl create ns pricetracker

Create 3 text files which store your database user, password and name. Secrets will be created out of these.
The files should be called

- POSTGRES_USER
- POSTGRES_DB
- POSTGRES_PASSWORD

kubectl create secret generic database --from-file=POSTGRES_PASSWORD=./POSTGRES_PASSWORD --from-file=POSTGRES_USER=./POSTGRES_USER --from-file=POSTGRES_DB=./POSTGRES_DB -n pricetracker
