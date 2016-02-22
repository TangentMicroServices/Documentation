# Documentation

Slate style documentation for MicroServices. 

## To run the installation: 

**Build the container**
```
docker build -t apidocs .
```

**Run the docs**

```
docker run -d -p 4567:4567 -v `pwd`:/app/source --name=apidocs apidocs
```

* map current host directory to `/app/source`
* name is `apidocs`

You should now be able to see it on: `http://docker-machine-ip:4567`

**Apply local changes**

To apply local changes you've made to the markdown, you will need to restart the container:

```
docker restart apidocs
```

et wala