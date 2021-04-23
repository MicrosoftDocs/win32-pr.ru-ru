---
title: Маршрутизация входящих запросов
description: API сервера HTTP поддерживает базу данных маршрутизации, чтобы определить, какое приложение получает входящий запрос.
ms.assetid: 7c613137-66bd-4375-93cb-b5562823bc12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da483030441f3a9239eef153da59212166bce9eb
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "104414080"
---
# <a name="routing-incoming-requests"></a><span data-ttu-id="538d9-103">Маршрутизация входящих запросов</span><span class="sxs-lookup"><span data-stu-id="538d9-103">Routing Incoming Requests</span></span>

<span data-ttu-id="538d9-104">API сервера HTTP поддерживает базу данных маршрутизации, чтобы определить, какое приложение получает входящий запрос.</span><span class="sxs-lookup"><span data-stu-id="538d9-104">The HTTP Server API maintains a routing database to determine which application receives an incoming request.</span></span> <span data-ttu-id="538d9-105">Таблица маршрутизации строится на основе базы данных резервирования и содержит записи резервирования, а также текущие регистрации.</span><span class="sxs-lookup"><span data-stu-id="538d9-105">The routing table is built from the reservation database and contains reservation entries as well as current registrations.</span></span> <span data-ttu-id="538d9-106">Когда выполняется регистрация или резервирование, оно помещается в контейнер базы данных маршрутизации, соответствующий типу узла, следующим образом:</span><span class="sxs-lookup"><span data-stu-id="538d9-106">When a registration or reservation is made, it is placed into the routing database bucket that corresponds to the host type as follows:</span></span>

-   <span data-ttu-id="538d9-107">\+ : регистрации портов помещаются в контейнер "строгий шаблон"</span><span class="sxs-lookup"><span data-stu-id="538d9-107">\+ : port registrations are placed in the "Strong Wildcard" bucket</span></span>

-   <span data-ttu-id="538d9-108">узел. регистрации портов помещаются в контейнер "explicit".</span><span class="sxs-lookup"><span data-stu-id="538d9-108">host : port registrations are placed in the "Explicit" bucket</span></span>

-   <span data-ttu-id="538d9-109">IP-адрес: регистрации портов помещаются в контейнер с слабым IP-адресом, связанным с системой</span><span class="sxs-lookup"><span data-stu-id="538d9-109">IP : port registrations are placed in the "IP-bound Weak Wildcard" bucket</span></span>

-   <span data-ttu-id="538d9-110">\* : регистрации портов помещаются в контейнер "слабый шаблон".</span><span class="sxs-lookup"><span data-stu-id="538d9-110">\* : port registrations are placed in the "Weak Wildcard" bucket</span></span>

<span data-ttu-id="538d9-111">Эти шаги также указывают на порядок обработки входящих HTTP-запросов.</span><span class="sxs-lookup"><span data-stu-id="538d9-111">These steps also refer to the order incoming HTTP requests are processed.</span></span> <span data-ttu-id="538d9-112">Сначала необходимо использовать строгие резервирования с подстановочными знаками, а затем явно зарезервированные данные, а также слабый подстановочный знак, связанный с IP-адресом.</span><span class="sxs-lookup"><span data-stu-id="538d9-112">The strong wildcard reservations first, then the explicit reservation are checked followed by the IP-bound weak wildcard and weak wildcard.</span></span> <span data-ttu-id="538d9-113">Поиск прекращается при обнаружении совпадения, чтобы регистрация в любом из оставшихся контейнеров не была найдена.</span><span class="sxs-lookup"><span data-stu-id="538d9-113">The search stops when a match is found so that registrations in any of the remaining buckets are not found.</span></span>

<span data-ttu-id="538d9-114">Алгоритм маршрутизации API HTTP-сервера находит наилучшее соответствие для [UrlPrefix](urlprefix-strings.md) , выполняя поиск по записям регистрации и записям резервирования базы данных маршрутизации, начиная с контейнера с строгим шаблоном и заканчивая слабым контейнером шаблона.</span><span class="sxs-lookup"><span data-stu-id="538d9-114">The HTTP Server API routing algorithm locates the best match for the [UrlPrefix](urlprefix-strings.md) by searching both the registration entries and the reservation entries of the routing database, starting with the strong wildcard bucket and ending with the weak wildcard bucket.</span></span> <span data-ttu-id="538d9-115">Наилучшее соответствие в контейнере — это самое длинное совпадение в относительной части URI UrlPrefix (при условии точного соответствия для частей адреса узла, порта и схемы).</span><span class="sxs-lookup"><span data-stu-id="538d9-115">The best match, within a bucket, is the longest match in the relative URI portion of the UrlPrefix (assuming an exact match for the host, port and scheme portions of the URL).</span></span> <span data-ttu-id="538d9-116">После обнаружения совпадения в контейнере алгоритм маршрутизации останавливает Поиск и пропускает все сегменты с более низким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="538d9-116">After a match is found in a bucket, the routing algorithm stops its search and skips all lower priority buckets.</span></span>

<span data-ttu-id="538d9-117">Например, рассмотрим следующие регистрации (перечисленные в порядке убывания приоритета на основе типов контейнеров:</span><span class="sxs-lookup"><span data-stu-id="538d9-117">For example, consider the following registrations (listed in descending order of priority based on bucket types:</span></span>

-   <span data-ttu-id="538d9-118">Регистрация: `https://+:80/vroot/` регистрируется приложением 1.</span><span class="sxs-lookup"><span data-stu-id="538d9-118">Registration: `https://+:80/vroot/` is registered by application 1</span></span>

-   <span data-ttu-id="538d9-119">Регистрация: `https://adatum.com:80/` регистрируется приложением 2.</span><span class="sxs-lookup"><span data-stu-id="538d9-119">Registration: `https://adatum.com:80/` is registered by application 2</span></span>

-   <span data-ttu-id="538d9-120">Регистрация: `https://\*:80/` регистрируется приложением 3.</span><span class="sxs-lookup"><span data-stu-id="538d9-120">Registration: `https://\*:80/` is registered by application 3</span></span>

<span data-ttu-id="538d9-121">Входящий запрос для `https://adatum.com:80/vroot/subdir/file.htm/` отправлен в приложение 1.</span><span class="sxs-lookup"><span data-stu-id="538d9-121">An incoming request for `https://adatum.com:80/vroot/subdir/file.htm/` is delivered to application 1.</span></span> <span data-ttu-id="538d9-122">Входящий запрос для `https://adatum.com:80/default.htm/` отправлен в приложение 2.</span><span class="sxs-lookup"><span data-stu-id="538d9-122">An incoming request for `https://adatum.com:80/default.htm/` is delivered to application 2.</span></span> <span data-ttu-id="538d9-123">Входящий запрос для `https://otheradatum.com:80/file.htm/` отправлен в приложение 3.</span><span class="sxs-lookup"><span data-stu-id="538d9-123">An incoming request for `https://otheradatum.com:80/file.htm/` is delivered to application 3.</span></span>

<span data-ttu-id="538d9-124">Если наиболее подходящее совпадение является записью резервирования, это означает, что приложение, которое должно получить запрос, не работает.</span><span class="sxs-lookup"><span data-stu-id="538d9-124">If the best match is a reservation entry, this means that the application that should receive the request is not running.</span></span> <span data-ttu-id="538d9-125">Например, рассмотрим следующую регистрацию и резервирование:</span><span class="sxs-lookup"><span data-stu-id="538d9-125">For example, consider the following registration and reservation:</span></span>

-   <span data-ttu-id="538d9-126">Регистрация: `https://\*:80/vroot/` регистрируется приложением 1, пользователем а</span><span class="sxs-lookup"><span data-stu-id="538d9-126">Registration: `https://\*:80/vroot/` is registered by application 1, user A</span></span>

-   <span data-ttu-id="538d9-127">Резервирование: `https://adatum.com:80/` зарезервировано для пользователя б</span><span class="sxs-lookup"><span data-stu-id="538d9-127">Reservation: `https://adatum.com:80/` has been reserved for user B</span></span>

<span data-ttu-id="538d9-128">Входящий запрос для `https://adatum.com:80/vroot/file.htm/` не доставляется в приложение 1, так как наилучшее соответствие приводит к записи резервирования для пользователя б. В этом случае к резервированию с более высоким приоритетом применяются правила приоритета.</span><span class="sxs-lookup"><span data-stu-id="538d9-128">An incoming request for `https://adatum.com:80/vroot/file.htm/` is not delivered to application 1 because the best match leads to the reservation entry for user B. The precedence rules are applied in this case to the reservation which has a higher priority.</span></span> <span data-ttu-id="538d9-129">Если нет активных процессов, которые были разрешены и зарегистрированы для запросов на обслуживание по полученному URL-адресу, запрос отклоняется с кодом состояния 400 (недопустимый запрос).</span><span class="sxs-lookup"><span data-stu-id="538d9-129">If no process is active that is authorized and registered to service requests for the URL received, the request is rejected with a 400 status code (Bad Request).</span></span>

 

 




