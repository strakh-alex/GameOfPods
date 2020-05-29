This is solution for the 1st lab of the Game Of Pods.

1. Start from drupal-mysql-secret.yml
  - kubectl create secret generic drupal-mysql-secret --from-literal=MYSQL_ROOT_PASSWORD=root_password --from-literal=MYSQL_DATABASE=drupal-database --from-literal=MYSQL_USER=root
2. Next read drupal-mysql-pv.yml and drupal-pv.yml
  - ssh node01
  - mkdir /drupal-data
  - chmod 777 /drupal-data
  - mkdir /drupal-mysql-data
  - chmod 777 /drupal-mysql-data
3. Then apply rest of the YAMLs