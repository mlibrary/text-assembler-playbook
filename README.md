## Before deploying
* Place an SSL private key file and matching SSL cert file inside `roles/apache/files`
* Copy `env.yml.example` to `env.yml` and fill in your variables
* Open `role/tassembler/templates/textassembler.cfg.example` and fill in your variables
* Open `role/apache/templates/tassembler.conf` and fill in your server url

## Ansible instructions
To test locally, run `vagrant up --provision`, and reset with `vagrant destroy`.

When everything seems nice and shiny, then you can deploy to whatever server you want to run this on. Put the IP address of your target server and `ansible_user=YOUR_USERNAME` into `/etc/ansible/hosts`. Ensure everything’s connected up right by running `ansible all -m ping`. A successful response will look something like this:
```
192.168.44.10 | SUCCESS => {
"changed": false, 
"failed": false, 
"ping": "pong"
}
```
