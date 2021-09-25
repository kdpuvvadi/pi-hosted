
# Pi-Hosted Ansible Playbook

This ansible Playbook is inspired by Don's [Novaspirit Tech](https://www.youtube.com/c/NovaspiritTech/) youtube series [pi-hosted](https://www.youtube.com/playlist?list=PL846hFPMqg3jwkxcScD1xw2bKXrJVvarc).

## Ansible Setup

Setup ansible environmint with docker SDK with follwoing.

1. Install pip `sudo apt install python3-pip -y`
2. install ansible with pip `pip install ansible`
3. Install docker sdk for ansible `pip install docker`
4. Install requirements `ansible-galaxy collection install -r requirements.yml`

## Clone the playbook

1. Clone the repo  `git clone https://github.com/kdpuvvadi/pi-hosted.git pi-hosted`.
2. copy inventory file with `cp inventory.ini.j2 inventory.ini`.
3. Change host ip of the host.
4. copy varible file with `cp vars.yml.j2` to `vars.yml.j2`.
5. Change the variable based on your preferences.

## Deployment

To deploy `pi-hosted` on raspberry-pi run

```bash
  ansible-playbook main.yml
```

Append `-K` if you need password for sudo access.

## List of Apps

* Docker and Portainer
* shell in a box
* Homer dashboard
* Guacamole

### Credentials

#### Guacamole

Default username and password both for guacamole are `guacadmin`

## Contributing

Contributions are always welcome!

clone the repo, modify the playbook and send a pull request.

## License

[MIT](https://choosealicense.com/licenses/mit/)
