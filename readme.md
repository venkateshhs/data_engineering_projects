docker run taxi_ingest:v001 --user=postgres --password=root --host=localhost --port=5432 --db=ny_taxi --table_name=yellow_taxi_trip --url="https://github.com/DataTalksClub/nyc-tlc-data/releases/download/yellow/yellow_tripdata_2021-01.csv.gz"
python ingest_data.py   --user=postgres   --password=root   --host=localhost   --port=5432   --db=ny_taxi   --table_name=yellow_taxi_trips   --url=${URL}

winpty docker run -it -e POSTGRES_USER="root" -e POSTGRES_PASSWORD="root" -e POSTGRES_DB="ny_taxi" -v c:/Users/Lenovo/Desktop/Venka Projects/data_engineering_projects:/var/lib/postgresql/data -p 5432:5432 --network=pg-network --name pg-database postgres:13

winpty docker run -it \
  -e POSTGRES_USER="root" \
  -e POSTGRES_PASSWORD="root" \
  -e POSTGRES_DB="ny_taxi" \
  -v /c/Users/Lenovo/Desktop/Venka Projects/data_engineering_projects:/var/lib/postgresql/data \
  -p 5432:5432 \
  --network=pg-network \
  --name pg-database2 \
  postgres:13




winpty docker run -it -e POSTGRES_USER="root" -e POSTGRES_PASSWORD="root" -e POSTGRES_DB="ny_taxi" -v /c/Users/Lenovo/Desktop/Venka\ Projects/data_engineering_projects:/var/lib/postgresql/data -p 5432:5432 --network=pg-network --name pg-database2 postgres:13



things learnt
pgadmin
docker
docker-compose
dockerfile
docker-compose.yaml
docker network
dcoker volume

 CORRECT VERSON
docker run -it -e POSTGRES_USER="root" -e POSTGRES_PASSWORD="root" -e POSTGRES_DB="ny_taxi" -v dtc_postgres_volume_local:/var/lib/postgresql/data -p 5432:5432 postgres:13
docker run -it -e POSTGRES_USER="root" -e POSTGRES_PASSWORD="root" -e POSTGRES_DB="ny_taxi" -v dtc_postgres_volume_local:/var/lib/postgresql/data -p 5432:5432 --network=pg-network --name=pg-databse postgres:13


docker run -it -e PGADMIN_DEFAULT_EMAIL="admin@admin.com" -e PGADMIN_DEFAULT_PASSWORD="root" -p 8080:80 --network=pg-network --name=pgadmin dpage/pgadmin4


python ingest_data.py --user=postgres --password=root --host=localhost --port=5432 --db=ny_taxi --table_name=yellow_taxi_trips --url="https://github.com/DataTalksClub/nyc-tlc-data/releases/download/yellow/yellow_tripdata_2021-01.csv.gz"

docker run -it --network=pg-network taxi_ingest:v001 --user=root --password=root --host=pg-databse --port=5432 --db=ny_taxi --table_name=yellow_taxi_trips --url="https://github.com/DataTalksClub/nyc-tlc-data/releases/download/yellow/yellow_tripdata_2021-01.csv.gz"
