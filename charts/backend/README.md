# Backend Helm Chart

## Installation

```sh
helm install [RELEASE_NAME] ./backend
```

## Removal                      
```bash                         
helm uninstall <release-name>   
```                             

## Environment Variables

The backend expects the following environment variables to be set:

| Variable               | Description                                      |
|------------------------|--------------------------------------------------|
| `MONGO_CONN_STR`       | MongoDB connection string                       |
| `MONGO_USERNAME`       | Username for MongoDB                            |
| `MONGO_PASSWORD`       | Password for MongoDB                            |
| `MONGO_AUTH_SOURCE`    | Authentication source for MongoDB               |

## Testing

```sh
curl http://<host>:9080
```
