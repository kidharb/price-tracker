1. Create a namespace called `pricetracker`

kubectl create ns pricetracker

Create 3 text files which store your database user, password and name. Secrets will be created out of these.
The files should be called

- db-user
- db-password
- db-name

kubectl create secret generic database \
    --from-file=username=./db-user \
    --from-file=password=./db-password \
    --from-file=database=./db-name
