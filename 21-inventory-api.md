---
title: Рекламный блок (Entity)
description: 
layout: libdoc/page

category: Inventory API
order: 21
---
* 
{:toc}

## Рекламный блок (Entity)

## Get All Entities
Получить все блоки
Запрос: GET: /inventory-api/entities
Ответ: JSON массив объектов Entity

## Create Entity
Создать инвентарь
Запрос: POST /inventory-api/entity/create
Тело запроса:  JSON объект Entity
Ответ: 200 OK empty body

## Read Entity
Получить блок по id
Запрос: GET /inventory-api/entity/read/{id}
Ответ: JSON объект Entity

## Update Entity
Обновить блок
Запрос: POST /inventory-api/entity/update
Тело запроса: JSON объект Entity
Ответ: 200 OK empty body

## Delete Entity
Удалить блок
Запрос: GET /inventory-api/entity/delete/{id}
Ответ: 200 OK empty body

