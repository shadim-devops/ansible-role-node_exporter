# Ansible Role: node_exporter

## Opis

Rola instaluje i konfiguruje Prometheus Node Exporter jako usługę systemd.
Umożliwia monitorowanie systemu przez Prometheus.

## Wymagania

- System Linux z systemd
- Uprawnienia sudo

## Zmienne (Role Variables)

| Zmienna | Opis | Domyślna wartość |
|----------|------|------------------|
| node_exporter_version | Wersja Node Exporter | 1.8.1 |
| node_exporter_port | Port nasłuchiwania | 9100 |
| node_exporter_user | Użytkownik systemowy | node-exp |
| node_exporter_group | Grupa systemowa | node-exp |
| node_exporter_install_dir | Katalog instalacji | /usr/local/bin |

## Przykład użycia

```yaml
- hosts: servers
  become: true
  roles:
    - shadim.node_exporter

