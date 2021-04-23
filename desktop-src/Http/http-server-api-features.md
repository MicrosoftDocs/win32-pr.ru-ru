---
title: Функции API сервера HTTP
description: В этом разделе поддерживались и не поддерживаются функции API-сервера HTTP.
ms.assetid: 448fe5a5-e79f-4c3a-aa76-94cff988f24f
keywords:
- Функции API сервера HTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48d5f529811b08999d6e1cfffa99fc85288ec471
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331915"
---
# <a name="http-server-api-features"></a><span data-ttu-id="90187-104">Функции API сервера HTTP</span><span class="sxs-lookup"><span data-stu-id="90187-104">HTTP Server API Features</span></span>

<span data-ttu-id="90187-105">В следующих списках описаны поддерживаемые и неподдерживаемые функции API-интерфейса сервера HTTP.</span><span class="sxs-lookup"><span data-stu-id="90187-105">The following lists describe supported and unsupported features of the HTTP Server API.</span></span>

## <a name="features-supported"></a><span data-ttu-id="90187-106">Поддерживаемые возможности</span><span class="sxs-lookup"><span data-stu-id="90187-106">Features Supported</span></span>

<span data-ttu-id="90187-107">Протокол HTTP поддерживает следующие функции:</span><span class="sxs-lookup"><span data-stu-id="90187-107">HTTP supports the following features:</span></span>

-   <span data-ttu-id="90187-108">Функции сервера HTTP v 1.0 и v 1.1.</span><span class="sxs-lookup"><span data-stu-id="90187-108">HTTP v1.0 and v1.1 server functionality.</span></span>
-   <span data-ttu-id="90187-109">SSL 3,0 (SSL) с поддержкой сертификатов клиента и сервера.</span><span class="sxs-lookup"><span data-stu-id="90187-109">Secure Sockets Layer 3.0 (SSL) with support for client and server certificates.</span></span>
-   <span data-ttu-id="90187-110">Кэширование фрагментов данных для использования в последующих ответах.</span><span class="sxs-lookup"><span data-stu-id="90187-110">Caching of data fragments for use in subsequent responses.</span></span>
-   <span data-ttu-id="90187-111">Поддержка адресации IPv6 и IPv4.</span><span class="sxs-lookup"><span data-stu-id="90187-111">Support for IPv6 and IPv4 addressing.</span></span>
-   <span data-ttu-id="90187-112">Резервирование пространства имен URL-адресов для безопасности приложения.</span><span class="sxs-lookup"><span data-stu-id="90187-112">URL namespace reservations for application security.</span></span>
-   <span data-ttu-id="90187-113">Истинные дескрипторы для всех объектов.</span><span class="sxs-lookup"><span data-stu-id="90187-113">True handles for all objects.</span></span>
-   <span data-ttu-id="90187-114">Синхронные и асинхронные модели ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="90187-114">Synchronous and asynchronous I/O models.</span></span>
-   <span data-ttu-id="90187-115">Поддержка WOW64 на компьютерах под управлением 64-разрядной версии Windows, начиная с Windows Server 2003 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="90187-115">Support for WOW64 on computers running on 64-bit Windows starting with Windows Server 2003 with Service Pack 1 (SP1).</span></span>

## <a name="features-not-supported"></a><span data-ttu-id="90187-116">Функции не поддерживаются</span><span class="sxs-lookup"><span data-stu-id="90187-116">Features Not Supported</span></span>

<span data-ttu-id="90187-117">API сервера HTTP не поддерживает следующие функциональные возможности:</span><span class="sxs-lookup"><span data-stu-id="90187-117">The HTTP Server API does not support the following functionality:</span></span>

-   <span data-ttu-id="90187-118">API сервера HTTP не выполняет проверку подлинности клиента или сервера на основе содержимого заголовков HTTP-запроса.</span><span class="sxs-lookup"><span data-stu-id="90187-118">The HTTP Server API does not perform client or server authentication based on the contents of the HTTP request headers.</span></span> <span data-ttu-id="90187-119">Все необходимые проверки подлинности должны быть реализованы приложением.</span><span class="sxs-lookup"><span data-stu-id="90187-119">Any required authentication must be implemented by the application.</span></span>
-   <span data-ttu-id="90187-120">Подсистема WOW64 на компьютерах под управлением 64-разрядной версии Windows не поддерживается в Windows Server 2003 и Windows XP с пакетом обновления 2 (SP2) и более ранних версий.</span><span class="sxs-lookup"><span data-stu-id="90187-120">WOW64 on computers running on 64-bit Windows is not supported on Windows Server 2003, and Windows XP with Service Pack 2 (SP2) and earlier.</span></span>
-   <span data-ttu-id="90187-121">API сервера HTTP не поддерживает ведение журнала HTTP-запросов и ответов.</span><span class="sxs-lookup"><span data-stu-id="90187-121">The HTTP Server API does not support logging HTTP requests and responses.</span></span>
-   <span data-ttu-id="90187-122">API-сервер HTTP не выполняет фрагментацию исходящих HTTP-ответов.</span><span class="sxs-lookup"><span data-stu-id="90187-122">The HTTP Server API does not chunk outgoing HTTP responses.</span></span> <span data-ttu-id="90187-123">При необходимости приложение должно реализовать фрагмент ответа.</span><span class="sxs-lookup"><span data-stu-id="90187-123">The application must implement response chunking if required.</span></span>

 

 




