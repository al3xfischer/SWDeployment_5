### Source
[Link](https://kubernetes.io/docs/tutorials/stateful-application/mysql-wordpress-persistent-volume/)

## URL to WP-Side
[Wordpress Website](http://52.155.238.200/)

## kustomization.yaml
Contains all the resources for deploying WordPress and a MYSQL database.
It also contains the password used withing Wordpress and MYSQL.

## mysql-deployment.yaml
The manifest describes a single-instance MySQL Deployment. The MySQL container mounts the PersistentVolume at /var/lib/mysql. The MYSQL_ROOT_PASSWORD environment variable sets the database password from the Secret.


## wordpress-deployment.yaml

The manifest describes a single-instance WordPress Deployment. The WordPress container mounts the PersistentVolume at /var/www/html for website data files. The WORDPRESS_DB_HOST environment variable sets the name of the MySQL Service defined above, and WordPress will access the database by Service. The WORDPRESS_DB_PASSWORD environment variable sets the database password from the Secret kustomize generated.

# How to deploy ?

Navigate to the folder with the files and execute the following command in your terminal:
```bash
kubectl apply -k ./
```