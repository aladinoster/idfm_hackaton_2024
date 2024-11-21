# idfm_hackaton_2024

## To Setup this project in Onyxia's VSCode
- Run:
```sh
git clone https://github.com/talan-tech-for-data/idfm_hackaton_2024.git .

sh -c "$(curl --location https://taskfile.dev/install.sh)" -- -d -b ~/.local/bin

sudo apt-get update -y
sudo apt-get install -y pipx

pipx install poetry

poetry config virtualenvs.in-project true

poetry install

cd frontend

curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.1/install.sh | bash

export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"  # This loads nvm
[ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion"  # This loads nvm bash_completion

nvm install 20

npm install

#npm run dev -- --host 0.0.0.0

#git submodule add https://github.com/IleDeFranceMobilites/hackathon_ia_mobilites_2024/
#git submodule update --init --remote # to pull from the hackaton repo
git submodule update --init

```

## To Install Sveltekit in Local Devcontainer or Github's devcontainer
### To start work, from zero:
- Run:

```bash

cd frontend

# install nvm
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.1/install.sh | bash

# activate nvm in current shell
export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"  # This loads nvm
[ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion"  # This loads nvm bash_completion

# install node 20
nvm install 20
# install project
npm install

npm run dev -- --open


```

### To Start dev in sveltekit:
```bash

cd frontend
# start the server and open the app in a new browser tab
npm run dev -- --open
```

### Other notes on sveltekit
```bash
nvm use 20
npm run build
```

```bash
npm run preview -- --open
```



## Other Notes
### When creating your vs code in onyxia, forward port 5173 for sveltekit
<img width="1163" alt="image" src="https://github.com/user-attachments/assets/48169289-48d4-4d5d-8d6f-9974da086ddd">


### To Install Windmill in Local devcontainer
Make sure Docker is started:

Mac: open /Applications/Docker.app
Windows: start docker
Linux: sudo systemctl start docker
and type the following commands:

```sh
cd windmill

# To start from scratch
#curl https://raw.githubusercontent.com/windmill-labs/windmill/main/docker-compose.yml -o docker-compose.yml
#curl https://raw.githubusercontent.com/windmill-labs/windmill/main/Caddyfile -o Caddyfile
#curl https://raw.githubusercontent.com/windmill-labs/windmill/main/.env -o .env

#docker compose up -d
docker compose -f windmill-docker-compose.yml up -d
```

Go to http://localhost on port 80
- _(Or equivalent in github devcontainer)_
![alt text](image.png)

Then you can login for the first time.

### opeenwebui
https://openwebui.com/assets/files/whitepaper.pdf

### port forwarding for sveltekit in local devcontainer
https://code.visualstudio.com/docs/devcontainers/containers#_always-forwarding-a-port


### In onyxia, Dev container extension won't work, because their current vscode implementation has Open Remote SSH off
![alt text](image-1.png)

### ALTERNATIVE? starting from vanilla sveltekit

npx sv create app
cd app
npm install
npm run dev
