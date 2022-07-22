# Melodistic Mono Repo

## Command

### Recursive Pull Submodule
`git pull --recurse-submodule`

### Deploy docker stack

`sudo docker-compose up -d`

`sudo docker stack deploy --compose-file docker-compose.yml melodisticmonorepo`

### Build and Push to ACR
```
sudo docker tag melodisticmonorepo_backend melodistic.azurecr.io/melodisticmonorepo_backend
sudo docker tag melodisticmonorepo_combiner-system melodistic.azurecr.io/melodisticmonorepo_combiner-system
sudo docker tag melodisticmonorepo_stream-backend melodistic.azurecr.io/melodisticmonorepo_stream-backend
sudo docker tag melodisticmonorepo_nginx melodistic.azurecr.io/melodisticmonorepo_nginx
sudo docker push melodistic.azurecr.io/melodisticmonorepo_backend
sudo docker push melodistic.azurecr.io/melodisticmonorepo_combiner-system
sudo docker push melodistic.azurecr.io/melodisticmonorepo_stream-backend
sudo docker push melodistic.azurecr.io/melodisticmonorepo_nginx
```