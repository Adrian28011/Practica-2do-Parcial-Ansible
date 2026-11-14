# Ansible Lab con Docker

## Objetivo de la práctica
Crear un laboratorio con dos servidores Linux utilizando Docker y administrarlos con Ansible.

## Iniciar los contenedores
```bash
docker compose up -d
docker ps
docker exec server1 bash -c "apt update && apt install -y python3"
docker exec server2 bash -c "apt update && apt install -y python3"
```

## Probar la conexión
```bash
ansible docker -i inventory.ini -m ping
```

## Ejecutar el playbook
```bash
ansible-playbook -i inventory.ini playbook.yml
```

## Captura de pantalla
![Ejecución exitosa del playbook](ansible_lab.png)
