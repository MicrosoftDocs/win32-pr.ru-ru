---
title: Модель программирования
description: Модель программирования API сервера HTTP включает пять групп действий.
ms.assetid: 8485cbdc-803f-4c10-ae4c-9ca53965d747
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30fe49dd9a50af72fc89efa6c10c56176966fda949fa177b3f081761a0d2a568
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014740"
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

 

 




