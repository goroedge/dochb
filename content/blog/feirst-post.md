---
# type: docs 
title: Как настроить HUGO?
slug: how-setup-hugo
date: 2024-10-25T12:40:21+03:00
featured: false
draft: false
comment: true
toc: true
reward: true
pinned: false
carousel: false
series: HUGO
categories: [site]
tags: [site]
images: []
---

Краткая инструкция по настройке и установки HUGO с темой 

<!--more-->

# Установим HUGO

## На Manjaro выполнить команду для загрузки из репозитория:
```shell
sudo pacman -S hugo   
```
## Установим язык GO, может поэтому он HUGO?
```shell
sudo pacman -S go
```
## Установить компиляторы C: GCC or Clang (они у меня уже были) 
## Загрузить последнюю версию HUGO и скомпилировать ее
```shell
CGO_ENABLED=1 go install -tags extended github.com/gohugoio/hugo@latest
```
## Проверить, что получилось
```shell 
hugo version
```

# Создать ключ доступа
```shell 
ssh-keygen -t ed25519 -C "sub@rabrain.ru"
```

Ключ будет в папке ~\.ssh

## Проверить настройки агента

```shell 
$ eval "$(ssh-agent -s)"
> Agent pid 59566
```

## Добавить ключ в агента
```shell 
ssh-add ~/.ssh/id_ed25519
```

## Добавить публичный ключ в настройки GitHub

# Клонировать репозиорий на диск
```shell 
$ git clone https://github.com/goroedge/myblog.git
```

## Выполнить NPM
```shell
$ npm ci
$ hugo server
```
