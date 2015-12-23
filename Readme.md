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

### Deploy to existing server

**:bangbang: You must have ssh access to the server**
```
./sync
cd epa-prototype-api
tape ansible deploy
```

### Provisioning a new server

**:bangbang: You must have ssh access to the server**

```
./sync
cd epa-prototype-api
```

1. Update the IP address in the `taperole/hosts` file to the IP address of your server.
2. Ensure you have ssh access as root to that server.
2. Ensure that Ubuntu 14.x LTS is the OS

```
tape ansible everything
```
