source : https://medium.com/@dataq/membuat-docker-private-registry-6efe534df4d5

how to install
--------------
1. Buka docker-compose.yml
2. Ubah "REGISTRY_HOST" menjadi IP Docker Private Registry
3. Run command dibawah untuk install registry dan ui

   $ docker-compose up -d

access
------

1. Agar kita bisa pull dari semua device, maka update (di setiap device) sebuah file yang berlokasi di :
   
   C:\Users\USER\.docker\daemon.json   ---> ON WINDOWS
   
   /etc/docker/daemon.json             ---> ON LINUX
 
   ATAU
   ----
   Masuk ke Docker Dekstop -> Setting -> Docker Engine        ---> ON WINDOWS

2. Tambahkan script berikut pada setiap device

   {
   "insecure-registries" : ["<ip_docker_private_registry>:5000"]
   }