---
title: Ведение журнала ошибок в API-интерфейсе HTTP-сервера
description: Некоторые типы ошибок обрабатываются API HTTP-сервера, а не передаются обратно приложению для обработки, так как в противном случае частота таких ошибок может привести к переполнению журнала событий или обработчика приложения.
ms.assetid: b919a718-e20b-4f34-a02e-bc028f8c32c7
keywords:
- API сервера HTTP, ведение журнала ошибок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d988d87a65c914625623c3f55d33a7f8cc9a4f94
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105681390"
---
# <a name="error-logging-in-the-http-server-api"></a><span data-ttu-id="bdf0b-104">Ведение журнала ошибок в API-интерфейсе HTTP-сервера</span><span class="sxs-lookup"><span data-stu-id="bdf0b-104">Error Logging in the HTTP Server API</span></span>

<span data-ttu-id="bdf0b-105">Некоторые типы ошибок обрабатываются API HTTP-сервера, а не передаются обратно приложению для обработки, так как в противном случае частота таких ошибок может привести к переполнению журнала событий или обработчика приложения.</span><span class="sxs-lookup"><span data-stu-id="bdf0b-105">Some kinds of errors are handled by the HTTP Server API rather than being passed back to an application for handling, because the frequency of such errors could otherwise flood an event log or application handler.</span></span>

<span data-ttu-id="bdf0b-106">В следующих трех разделах описаны различные аспекты ведения журнала ошибок API-сервера HTTP.</span><span class="sxs-lookup"><span data-stu-id="bdf0b-106">The following three topics describe the different aspects of the HTTP Server API error logging:</span></span>

-   <span data-ttu-id="bdf0b-107">[Конфигурация](configuring-http-server-api-error-logging.md) Параметры реестра контролируют, регистрирует ли API-сервер HTTP ошибки, максимально допустимый размер файлов журнала и место сохранения файлов журнала.</span><span class="sxs-lookup"><span data-stu-id="bdf0b-107">[Configuration](configuring-http-server-api-error-logging.md) Registry settings control whether the HTTP Server API logs errors, the maximum allowable size of log files, and where log files are saved.</span></span>
-   <span data-ttu-id="bdf0b-108">[Формат файла журнала](format-of-the-http-server-api-error-logs.md) API сервера HTTP создает файлы журналов, которые соответствуют соглашениям о файле журнала консорциум W3C (W3C) и могут быть проанализированы с помощью стандартных средств.</span><span class="sxs-lookup"><span data-stu-id="bdf0b-108">[Log File Format](format-of-the-http-server-api-error-logs.md) The HTTP Server API creates log files that comply with the World Wide Web Consortium (W3C) log file conventions, and can be parsed by using standard tools.</span></span> <span data-ttu-id="bdf0b-109">Однако, в отличие от файлов журнала W3C, файлы журнала API HTTP-сервера не содержат имен столбцов.</span><span class="sxs-lookup"><span data-stu-id="bdf0b-109">However, unlike W3C log files, HTTP Server API log files do not contain names of the columns.</span></span>
-   <span data-ttu-id="bdf0b-110">[Типы регистрируемых ошибок](types-of-errors-logged-by-the-http-server-api.md) API сервера HTTP регистрирует различные распространенные ошибки.</span><span class="sxs-lookup"><span data-stu-id="bdf0b-110">[Types of Errors Logged](types-of-errors-logged-by-the-http-server-api.md) The HTTP Server API logs a variety of common errors.</span></span>

 

 




