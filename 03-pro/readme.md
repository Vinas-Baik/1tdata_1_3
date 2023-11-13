1. создать докер образ базы данных из папки db следующим командами
   - docker build -t 1tdata_1_3_03_db:latest .
2. создать контейнер на основе образа с подключением тома
   - docker run -p 5432:5432 --name 1tdata_03_db_con -v /data:/var/lib/postgresql/data -d 1tdata_1_3_03_db:latest
3. подключиться к контейнерыу базы данных, посмотреть данные
   - docker exec -it 1tdata_03_db_con psql -U postgres
4. создать докер образ программы из папки app
   - docker build -t 1tdata_1_3_03_pro_app:latest .
5. создать контейнер на основе образа
   - docker run --name 1tdata_03_app_con -d 1tdata_1_3_03_pro_app:latest
7. проверить работу программы
   - docker exec -it 1tdata_03_app_con python
