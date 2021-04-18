---
title: Модель программирования
description: Модель программирования API сервера HTTP включает пять групп действий.
ms.assetid: 8485cbdc-803f-4c10-ae4c-9ca53965d747
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: def54ac8a34d6c53ea4e2825ef39884f0141df99
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/06/2021
ms.locfileid: "104562007"
---
# <a name="programming-model"></a>Модель программирования

Модель программирования API сервера HTTP включает пять групп действий:

-   [Настройка конфигурации](setup-configuration.md)
-   [Конфигурация среды выполнения](run-time-configuration.md)
-   [Создание очереди запросов и привязка к ней](creating-and-binding-to-a-request-queue.md)
-   [Обработка запросов](processing-requests.md)
-   [Завершение работы и очистка](shutdown-and-cleanup.md)

![Схема, на которой показана модель программирования P I t t P Server.](images/http-server-api-programming-model.png)

Пример приложения, в котором показано, как выполнять действия HTTP GET и POST Request и как отправить сообщение об ошибке 503 (**не \_ реализовано**), если в запросе, который не обрабатывается приложением, есть действия, см. в разделе [пример приложения HTTP-сервера](http-server-sample-application.md).

 

 




