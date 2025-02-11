# PostgreSQL

bash
```
brew services stop postgresql@14
brew services start postgresql@14
```
After starting 
If the database does not exist then do this :

If database and table both are there :
bash
```
psql -U postgres -d tweet_events
```

If you want to exit the postgres:
bash
```
\q
```
