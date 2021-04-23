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
# <a name="programming-model"></a><span data-ttu-id="f6a6e-103">Модель программирования</span><span class="sxs-lookup"><span data-stu-id="f6a6e-103">Programming Model</span></span>

<span data-ttu-id="f6a6e-104">Модель программирования API сервера HTTP включает пять групп действий:</span><span class="sxs-lookup"><span data-stu-id="f6a6e-104">The HTTP Server API programming model includes five groups of activities:</span></span>

-   [<span data-ttu-id="f6a6e-105">Настройка конфигурации</span><span class="sxs-lookup"><span data-stu-id="f6a6e-105">Setup configuration</span></span>](setup-configuration.md)
-   [<span data-ttu-id="f6a6e-106">Конфигурация среды выполнения</span><span class="sxs-lookup"><span data-stu-id="f6a6e-106">Run-time configuration</span></span>](run-time-configuration.md)
-   [<span data-ttu-id="f6a6e-107">Создание очереди запросов и привязка к ней</span><span class="sxs-lookup"><span data-stu-id="f6a6e-107">Creating and binding to a request queue</span></span>](creating-and-binding-to-a-request-queue.md)
-   [<span data-ttu-id="f6a6e-108">Обработка запросов</span><span class="sxs-lookup"><span data-stu-id="f6a6e-108">Processing requests</span></span>](processing-requests.md)
-   [<span data-ttu-id="f6a6e-109">Завершение работы и очистка</span><span class="sxs-lookup"><span data-stu-id="f6a6e-109">Shutdown and cleanup</span></span>](shutdown-and-cleanup.md)

![Схема, на которой показана модель программирования P I t t P Server.](images/http-server-api-programming-model.png)

<span data-ttu-id="f6a6e-111">Пример приложения, в котором показано, как выполнять действия HTTP GET и POST Request и как отправить сообщение об ошибке 503 (**не \_ реализовано**), если в запросе, который не обрабатывается приложением, есть действия, см. в разделе [пример приложения HTTP-сервера](http-server-sample-application.md).</span><span class="sxs-lookup"><span data-stu-id="f6a6e-111">For a sample application that shows how to handle the HTTP GET and POST request actions and how to send a 503 (**NOT\_IMPLEMENTED**) error if actions are present in the request that the application does not handle, see [HTTP Server Sample Application](http-server-sample-application.md).</span></span>

 

 




