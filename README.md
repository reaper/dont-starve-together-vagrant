# dont-starve-together-vagrant
Don't Starve Together vagrant with docker provider

## Preparation steps
```
git clone https://github.com/reaper/dont-starve-together-vagrant-docker
cd dont-starve-together-vagrant-docker
cp settings.ini.example settings.ini
cp dedicated_server_mods_setup.lua.example dedicated_server_mods_setup.lua
printf DONT_STARVE_TOGETHER_TOKEN'\0' > server_token.txt     # Don't forget unix null char EOL
```

Edit settings.ini as your convenance to configure your server.

Edit dedicated_server_mods_setup.lua and add your mods (READ header comments to know how to add mods)

## Startup
```
vagrant up --provider=docker
vagrant ssh
./start_dst.sh
```
