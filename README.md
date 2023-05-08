# API do site PET-AMIGO
Esse documento descreve os passos necessários para a criação do ambiente de desenvolvimento e manutenção das APIs do projeto.

## Requisitos
Os requisitos necessários para o acesso as funcionalidades do projeto são o Python na versão 3.8 juntamente com o pip 20.0.2 (versão que vem em conjunto com o python 3.8)

## Inicializando o projeto
É preciso baixar a biblioteca para criar o ambiente virtual do Django, com o comando 
```
pip3 install virtualenv
```
Após isso caso esteja usando ubuntu ou alguma distribuição linux é possivel iniciar o ambiente com:
```
. ./bin/setup_env_ubuntu.sh  
```
Caso contrario use 
```
python3 -m venv venv
pip3 install -r requirements.txt
```
Com isso todas as dependencias do projeto estão configuradas, agora use:
```
python3 manage.py migrate --settings=petamigo.settings.development
```
o "--settings=petamigo.settings.development" é necessario para rodar o comando com as configurações de desenvolvimento, quando for iniciar em produção use "--settings=petamigo.settings.production", por fim, é póssivel iniciar o servidor do backend com 
```
python3 manage.py runserver --settings=petamigo.settings.development
```
