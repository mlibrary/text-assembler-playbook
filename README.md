## Before deploying
* Place an SSL private key file and matching SSL cert file inside `roles/apache/files`
* Copy `env.yml.example` to `env.yml` and fill in your variables
* Open `role/tassembler/templates/textassembler.cfg.example` and fill in your variables
* Open `role/apache/templates/tassembler.conf` and fill in your server url
