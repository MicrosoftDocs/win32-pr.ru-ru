---
description: Схема для отчетов об ошибках отличается между интерфейсами SPI и API.
ms.assetid: f4a4b406-3e3a-444f-b75a-0cf51bded1bc
title: Отчеты об ошибках и проверка параметров
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 291fa2ed950d916be39b1a696f5fe8ad6f07280c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701536"
---
# <a name="error-reporting-and-parameter-validation"></a><span data-ttu-id="12d94-103">Отчеты об ошибках и проверка параметров</span><span class="sxs-lookup"><span data-stu-id="12d94-103">Error Reporting and Parameter Validation</span></span>

<span data-ttu-id="12d94-104">Схема для отчетов об ошибках отличается между интерфейсами SPI и API.</span><span class="sxs-lookup"><span data-stu-id="12d94-104">The scheme for error reporting differs between the SPI and API interfaces.</span></span> <span data-ttu-id="12d94-105">Поставщики служб Windows Sockets сообщают об ошибках вместе с возвратом функции, в отличие от подхода, основанного на потоках, который используется в API.</span><span class="sxs-lookup"><span data-stu-id="12d94-105">Windows Sockets service providers report errors along with the function returning, as opposed to the per-thread based approach utilized in the API.</span></span> <span data-ttu-id="12d94-106">32.dll Ws2 \_ использует код ошибки для каждой функции поставщика услуг, чтобы обновить значение ошибки потока, полученное с помощью функции API [**всажетластеррор**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) .</span><span class="sxs-lookup"><span data-stu-id="12d94-106">The Ws2\_32.dll uses the service provider's per-function error code to update the per-thread error value that is obtained through the [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) API function.</span></span> <span data-ttu-id="12d94-107">Однако поставщики услуг по-прежнему требуются для поддержания ошибок на основе сокетов, которые можно получить с помощью параметра, чтобы использовать \_ сокет с ошибками.</span><span class="sxs-lookup"><span data-stu-id="12d94-107">Service providers are still required, however, to maintain the per-socket based error which can be retrieved through the SO\_ERROR socket option.</span></span>

<span data-ttu-id="12d94-108">32.dll Ws2 \_ выполняет проверку параметров только для вызовов функций, реализованных полностью внутри самой себя.</span><span class="sxs-lookup"><span data-stu-id="12d94-108">The Ws2\_32.dll performs parameter validation only on function calls that are implemented entirely within itself.</span></span> <span data-ttu-id="12d94-109">Поставщики услуг отвечают за выполнение всех собственных проверок параметров.</span><span class="sxs-lookup"><span data-stu-id="12d94-109">Service providers are responsible for performing all of their own parameter validation.</span></span>

 

 



