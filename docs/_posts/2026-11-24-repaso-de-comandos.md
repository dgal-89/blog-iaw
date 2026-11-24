---
layout: post
title: "Repaso de comandos"
---

## Terminal

- mkdir carpeta: crear una carpeta
- cd carpeta: entrar en una carpeta
- ls -la: ver todo lo que hay en la carpeta, también lo oculto

## Git

- git init: crear el repositorio
- git config --global user.name "Nombre": poner tu nombre
- git config --global user.email "correo": poner tu email
- git config user.name: ver el nombre que tienes puesto
- git config user.email: ver el email que tienes puesto
- git add archivo: preparar un archivo
- git add archivo1 archivo2: preparar varios archivos
- git add .: preparar todo
- git status: ver cómo están los archivos
- git rm --cached archivo: quitar un archivo de lo preparado sin borrarlo
- git rm --cached . -r: quitar todo de lo preparado
- git commit -m "mensaje": guardar los cambios
- git log: ver los commits que has hecho
- git diff: ver qué has cambiado

## Ramas

- git branch: ver las ramas
- git switch -c rama: crear una rama y meterte en ella
- git checkout -b rama: lo mismo pero a la antigua
- git switch main: volver a main
- git checkout main: lo mismo pero a la antigua
- git merge rama: juntar esa rama con la que estás
- git branch -M main: cambiar el nombre de la rama a main

## GitHub

- git clone URL: descargar un repositorio
- git remote add origin URL: conectar tu carpeta con GitHub
- git remote -v: ver a qué repositorio está conectada
- git push -u origin main: subir los cambios la primera vez
- git push: subir los cambios
- git pull: bajar los cambios

## Docker

- docker compose config --quiet: comprobar que el archivo docker-compose.yml está bien
- docker compose up -d: arrancar el contenedor
- http://localhost:4000: dirección para ver la web en el navegador

## Jekyll

Estos comandos van dentro del docker-compose.yml y se ejecutan solos al arrancar el contenedor:

- gem install jekyll --version 3.10.0: instalar Jekyll
- jekyll new docs --skip-bundle: crear la web en la carpeta docs
- bundle check: comprobar si están las dependencias
- bundle install: instalar las dependencias
- bundle exec jekyll serve: arrancar la web

## Subir la web a GitHub

- git init: crear el repositorio
- git add .gitignore docs docker-compose.yml: preparar los archivos de la web
- git commit -m "mensaje": guardar los cambios
- git branch -M main: cambiar el nombre de la rama a main
- git remote add origin URL: conectar la carpeta con GitHub
- git push -u origin main: subir la web
- git add docs/_config.yml: preparar el archivo con las rutas arregladas
- git commit -m "mensaje": guardar el cambio
- git push: subir el cambio

Para publicarla: Settings, Pages, rama main y carpeta /docs.