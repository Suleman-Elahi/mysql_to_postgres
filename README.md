Migrating the Mysql Database to Postgres Database

mysqldump --compatible=postgresql --default-character-set=utf8 -r <databasename>.mysql -u root <databasename>
  
chmod +rx dbconverter.py

python dbconverter.py <databasename>.mysql <databasename>.psql
    
psql databasename -U postgres -h 127.0.0.1 < <databasename>.psql
