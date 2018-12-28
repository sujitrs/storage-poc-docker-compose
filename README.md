# storage-poc-docker-compose

docker run -p 7171:7171 ms-app-repo-docker:latest --entrypoint "java -cp app:app/lib/* -Dspring.profiles.active=development -Dspring.datasource.url=jdbc:postgresql://172.19.69.95:5434/postgres -Dspring.datasource.username=postgres -Dspring.datasource.password=nsdl1234 org.sj.msapprepo.MsAppRepoApplication"

docker run -p 9000:9191 ms-user-repo-docker:latest --entrypoint "java -cp app:app/lib/* -Dspring.profiles.active=development -Dspring.datasource.url=jdbc:postgresql://172.19.69.95:5434/postgres -Dspring.datasource.username=postgres -Dspring.datasource.password=nsdl1234 org.sj.msuserrepo.MsUserRepoApplication"

docker run -p 8000:8181 ms-file-mgmt-docker:latest --entrypoint "java -cp app:app/lib/* -Dspring.profiles.active=development -Dspring.datasource.url=jdbc:postgresql://172.19.69.95:5434/postgres -Dspring.datasource.username=postgres -Dspring.datasource.password=nsdl1234 org.sj.msfilemgmnt.MsFileMgmntApplication"

