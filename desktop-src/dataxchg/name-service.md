---
title: Служба имен
description: В этом разделе описано, как библиотека управления платформа динамических данных Exchange позволяет серверному приложению регистрировать имена служб, которые она поддерживает.
ms.assetid: 4b7e7f43-18aa-4c2e-aa2b-5ce7bb18048f
keywords:
- Пользовательский интерфейс Windows, платформа динамических данных Exchange (DDE)
- Платформа динамических данных Exchange (DDE), служба имен
- DDE (платформа динамических данных Exchange), служба имен
- Обмен данными, платформа динамических данных Exchange (DDE)
- Пользовательский интерфейс Windows, Библиотека управления платформа динамических данных Exchange (ДДЕМЛ)
- Библиотека управления платформа динамических данных Exchange (ДДЕМЛ), служба имен
- ДДЕМЛ (Библиотека управления Exchange платформа динамических данных), служба имен
- Обмен данными, Библиотека управления платформа динамических данных Exchange (ДДЕМЛ)
- Платформа динамических данных Exchange (DDE), регистрация имени службы
- DDE (платформа динамических данных Exchange), регистрация имени службы
- Библиотека управления платформа динамических данных Exchange (ДДЕМЛ), регистрация имени службы
- ДДЕМЛ (платформа динамических данных Библиотека управления Exchange), регистрация имени службы
- Платформа динамических данных Exchange (DDE), фильтр имен служб
- DDE (платформа динамических данных Exchange), фильтр имен служб
- Библиотека управления платформа динамических данных Exchange (ДДЕМЛ), фильтр имен служб
- ДДЕМЛ (Библиотека управления Exchange платформа динамических данных), фильтр имен служб
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10f958ab73164e70177cb5deeb5f400f44695015
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332627"
---
# <a name="name-service"></a><span data-ttu-id="03eae-119">Служба имен</span><span class="sxs-lookup"><span data-stu-id="03eae-119">Name Service</span></span>

<span data-ttu-id="03eae-120">Платформа динамических данных Библиотека управления Exchange (ДДЕМЛ) позволяет серверному приложению регистрировать имена служб, которые она поддерживает, и предотвращать отправку ДДЕМЛ [**кстип \_ Connect**](xtyp-connect.md) Transactions для неподдерживаемых имен служб в функцию обратного вызова Exchange Server Платформа динамических данных (DDE).</span><span class="sxs-lookup"><span data-stu-id="03eae-120">The Dynamic Data Exchange Management Library (DDEML) makes it possible for a server application to register the service names that it supports and to prevent the DDEML from sending [**XTYP\_CONNECT**](xtyp-connect.md) transactions for unsupported service names to the server's Dynamic Data Exchange (DDE) callback function.</span></span>

<span data-ttu-id="03eae-121">В следующих разделах описывается служба имен.</span><span class="sxs-lookup"><span data-stu-id="03eae-121">The following topics describe the name service.</span></span>

-   [<span data-ttu-id="03eae-122">Регистрация имени службы</span><span class="sxs-lookup"><span data-stu-id="03eae-122">Service Name Registration</span></span>](#service-name-registration)
-   [<span data-ttu-id="03eae-123">Фильтр имени службы</span><span class="sxs-lookup"><span data-stu-id="03eae-123">Service Name Filter</span></span>](#service-name-filter)

## <a name="service-name-registration"></a><span data-ttu-id="03eae-124">Регистрация имени службы</span><span class="sxs-lookup"><span data-stu-id="03eae-124">Service Name Registration</span></span>

<span data-ttu-id="03eae-125">Регистрируя имена служб в ДДЕМЛ, сервер информирует другие приложения DDE в системе о том, что новый сервер доступен.</span><span class="sxs-lookup"><span data-stu-id="03eae-125">By registering its service names with the DDEML, a server informs other DDE applications in the system that a new server is available.</span></span> <span data-ttu-id="03eae-126">Сервер регистрирует имя службы с помощью вызова функции [**дденамесервице**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) и указания строкового маркера, определяющего имя.</span><span class="sxs-lookup"><span data-stu-id="03eae-126">A server registers a service name by calling the [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) function and specifying a string handle that identifies the name.</span></span> <span data-ttu-id="03eae-127">В ответ ддемл отправляет транзакцию [**\_ регистра кстип**](xtyp-register.md) в функцию обратного вызова каждого приложения ддемл в системе (за исключением тех, которые указали флаг фильтра КБФ Registering \_ \_ в функции [**ддеинитиализе**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) ).</span><span class="sxs-lookup"><span data-stu-id="03eae-127">In response, the DDEML sends an [**XTYP\_REGISTER**](xtyp-register.md) transaction to the callback function of each DDEML application in the system (except those that specified the CBF\_SKIP\_REGISTRATIONS filter flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function).</span></span> <span data-ttu-id="03eae-128">Транзакция **кстип \_ Register** передает в функцию обратного вызова два дескриптора строки: первый определяет строку, указывающую базовое имя службы, а вторая определяет строку, указывающую на конкретную службу экземпляра.</span><span class="sxs-lookup"><span data-stu-id="03eae-128">The **XTYP\_REGISTER** transaction passes two string handles to a callback function: the first identifies the string specifying the base service name, and the second identifies the string specifying the instance-specific service.</span></span> <span data-ttu-id="03eae-129">Клиент обычно использует имя базовой службы в списке доступных серверов, чтобы пользователь мог выбрать сервер из списка.</span><span class="sxs-lookup"><span data-stu-id="03eae-129">A client typically uses the base service name in a list of available servers, so the user can select a server from the list.</span></span> <span data-ttu-id="03eae-130">Клиент использует имя службы для конкретного экземпляра, чтобы установить диалог с конкретным экземпляром серверного приложения, если выполняется более одного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="03eae-130">The client uses the instance-specific service name to establish a conversation with a specific instance of a server application, if more than one instance is running.</span></span>

<span data-ttu-id="03eae-131">Сервер может использовать [**дденамесервице**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) для отмены регистрации имени службы.</span><span class="sxs-lookup"><span data-stu-id="03eae-131">A server can use [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) to unregister a service name.</span></span> <span data-ttu-id="03eae-132">Эта функция заставляет ДДЕМЛ отсылать [**КСТИП \_ отмену регистрации**](xtyp-unregister.md) транзакций в другие приложения DDE в системе, уведомляя их о том, что они больше не могут использовать имя для установки диалогов.</span><span class="sxs-lookup"><span data-stu-id="03eae-132">This function causes the DDEML to send [**XTYP\_UNREGISTER**](xtyp-unregister.md) transactions to the other DDE applications in the system, informing them that they can no longer use the name to establish conversations.</span></span>

<span data-ttu-id="03eae-133">Сервер должен вызвать [**дденамесервице**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) для регистрации имен служб вскоре после вызова [**ддеинитиализе**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea).</span><span class="sxs-lookup"><span data-stu-id="03eae-133">A server must call [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) to register its service names soon after calling [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea).</span></span> <span data-ttu-id="03eae-134">Сервер должен отменить регистрацию своих имен служб с помощью **дденамесервице** непосредственно перед вызовом функции [**ддеунинитиализе**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize) .</span><span class="sxs-lookup"><span data-stu-id="03eae-134">A server must unregister its service names by using **DdeNameService** just before calling the [**DdeUninitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize) function.</span></span>

## <a name="service-name-filter"></a><span data-ttu-id="03eae-135">Фильтр имени службы</span><span class="sxs-lookup"><span data-stu-id="03eae-135">Service Name Filter</span></span>

<span data-ttu-id="03eae-136">Помимо регистрации имен служб, [**дденамесервице**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) позволяет серверу включить или отключить фильтрацию имени службы.</span><span class="sxs-lookup"><span data-stu-id="03eae-136">In addition to registering service names, [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) enables a server to turn its service name filter on or off.</span></span> <span data-ttu-id="03eae-137">Когда сервер выключает фильтр имени службы, ДДЕМЛ отправляет транзакцию [**кстип \_ Connect**](xtyp-connect.md) в функцию обратного вызова DDE сервера, когда любой клиент вызывает функцию [**ддеконнект**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) , независимо от имени службы, указанного в функции.</span><span class="sxs-lookup"><span data-stu-id="03eae-137">When a server turns off its service name filter, the DDEML sends the [**XTYP\_CONNECT**](xtyp-connect.md) transaction to the server's DDE callback function whenever any client calls the [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) function, regardless of the service name specified in the function.</span></span> <span data-ttu-id="03eae-138">Когда сервер включает фильтр имени службы, ДДЕМЛ отправляет транзакцию **кстип \_ Connect** на сервер, только если **ддеконнект** указывает имя службы, указанное сервером при вызове **дденамесервице**.</span><span class="sxs-lookup"><span data-stu-id="03eae-138">When a server turns on its service name filter, the DDEML sends the **XTYP\_CONNECT** transaction to the server only when **DdeConnect** specifies a service name the server has specified in a call to **DdeNameService**.</span></span>

<span data-ttu-id="03eae-139">По умолчанию фильтр имен служб включен, когда приложение вызывает [**ддеинитиализе**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea).</span><span class="sxs-lookup"><span data-stu-id="03eae-139">By default, the service name filter is on when an application calls [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea).</span></span> <span data-ttu-id="03eae-140">Это значение по умолчанию предотвращает отправку ДДЕМЛ транзакции [**кстип \_ Connect**](xtyp-connect.md) на сервер до того, как сервер создаст необходимые ему дескрипторы строк.</span><span class="sxs-lookup"><span data-stu-id="03eae-140">This default prevents the DDEML from sending the [**XTYP\_CONNECT**](xtyp-connect.md) transaction to a server before the server has created the string handles it needs.</span></span> <span data-ttu-id="03eae-141">Сервер может отключить фильтр имени службы, указав \_ флаг DNS филтерофф в вызове [**дденамесервице**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice).</span><span class="sxs-lookup"><span data-stu-id="03eae-141">A server can turn off its service name filter by specifying the DNS\_FILTEROFF flag in a call to [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice).</span></span> <span data-ttu-id="03eae-142">\_Флаг ФИЛЬТРАЦИИ DNS включает фильтр.</span><span class="sxs-lookup"><span data-stu-id="03eae-142">The DNS\_FILTERON flag turns on the filter.</span></span>

 

 




