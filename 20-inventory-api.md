---
title: Рекламный инвентарь (Inventory)
description: 
layout: libdoc/page

category: Inventory API
order: 20
---
* 
{:toc}

## Рекламный инвентарь (Inventory)

## Get All Inventories
Получить весь инвентарь
Запрос: GET: /inventory-api/inventories
Ответ: JSON массив объектов Inventory

## Create Inventory
Создать инвентарь
Запрос: POST /inventory-api/inventory/create
Тело запроса:  JSON объект Inventory 
Ответ: 200 OK empty body

## Read Inventory
Получить инвентарь по id
Запрос: GET /inventory-api/inventory/read/{id}
Ответ: JSON объект Inventory

## Update Inventory
Обновить инвентарь
Запрос: POST /inventory-api/inventory/update
Тело запроса: JSON объект Inventory
Ответ: 200 OK empty body

## Delete Inventory
Удалить инвентарь
Запрос: GET /inventory-api/inventory/delete/{id}
Ответ: 200 OK empty body

