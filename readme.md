
Creating an pushing a container
-------------------------------

This folder creates a container running WP in non root, on port 8080.
* Includes wp-cli so that cli commands can be issued within the container.
* This version of the dockerfile also installs a nodejs service inside the container


Link to DO Container Registry: https://www.digitalocean.com/products/container-registry


Commands to build and push the container
```
sudo docker build -t registry.digitalocean.com/locol-core/locol-wp:22-01-15a .

sudo docker push registry.digitalocean.com/locol-core/locol-wp:22-01-15a
```

WP CLI command to rename site name
```
wp search-replace 'uat-cloud.locol.media' 'www.locol.media' --dry-run --allow-root
```