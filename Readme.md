#EPA Prototype

**[Android](https://github.com/smashingboxes/epa-prototype-android)**
**[Frontend](https://github.com/smashingboxes/epa-prototype-frontend)**
**[API](https://github.com/smashingboxes/epa-prototype-api)**

## How to synchronize scripts

```
./sync
```

## Deployment

This application uses [Anisble](http://www.ansible.com/) for server management and application deployment.

### Deploy to existing servier

**:bangbang: you must have ssh access to the server**
```
./sync
cd epa-prototype-api
tape ansible deploy
```
