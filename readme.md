# Ansible

## testiranje pomocu "ping" gde je iz ansible direktorijuma:
### inventory file rucno unet: -i inventory.yml
### srbija lokacija iz inventory.yml
### user na VMu: inventory.yml
### modul: -m ping
### rucno unt ssh keyfile (iz direktorijuma gde za terraform)
ansible srbija -i inventory.yml -u ubuntu -m ping --key-file ~/local/.ssh/id_ed25519

## instalacija dockera
### iz ansible direktorijuma
### pod variablom "host" uneti grupu iz onventory fajla
ansible-playbook -i inventory.yml playbooks/install_docker.yml -u ubuntu --extra-vars "host=beograd"

## instalacija nginx
### iz ansible direktorijuma
### pod variablom "host" uneti grupu iz onventory fajla
ansible-playbook -i inventory.yml playbooks/install_nginx.yml -u ubuntu --extra-vars "host=beograd"


