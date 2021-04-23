---
title: Функции API сервера HTTP версии 1,0
description: API сервера HTTP предоставляет следующие функции для создания приложений.
ms.assetid: 1da9907d-a09d-41e1-aca1-9a8e2b91296f
keywords:
- Функции API сервера HTTP версии 1,0
- Функции HTTP, API HTTP-сервера версии 1,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 050821e40695268d6e3fa2c946d2e8859748db2b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104258854"
---
# <a name="http-server-api-version-10-functions"></a><span data-ttu-id="d6598-105">Функции API сервера HTTP версии 1,0</span><span class="sxs-lookup"><span data-stu-id="d6598-105">HTTP Server API Version 1.0 Functions</span></span>

<span data-ttu-id="d6598-106">API сервера HTTP предоставляет следующие функции для создания приложений.</span><span class="sxs-lookup"><span data-stu-id="d6598-106">The HTTP Server API provides the following functions for writing applications.</span></span>

## <a name="general"></a><span data-ttu-id="d6598-107">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="d6598-107">General</span></span>



| <span data-ttu-id="d6598-108">Функция</span><span class="sxs-lookup"><span data-stu-id="d6598-108">Function</span></span>                                             | <span data-ttu-id="d6598-109">Описание</span><span class="sxs-lookup"><span data-stu-id="d6598-109">Description</span></span>                                                                                                                       |
|------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d6598-110">**хттпкреатехттфандле**</span><span class="sxs-lookup"><span data-stu-id="d6598-110">**HttpCreateHttpHandle**</span></span>](/windows/desktop/api/Http/nf-http-httpcreatehttphandle) | <span data-ttu-id="d6598-111">Создает очередь HTTP-запросов и возвращает к ней маркер.</span><span class="sxs-lookup"><span data-stu-id="d6598-111">Creates an HTTP request queue and returns a handle to it.</span></span>                                                                         |
| [<span data-ttu-id="d6598-112">**хттпинитиализе**</span><span class="sxs-lookup"><span data-stu-id="d6598-112">**HttpInitialize**</span></span>](/windows/desktop/api/Http/nf-http-httpinitialize)             | <span data-ttu-id="d6598-113">Инициализирует API HTTP-сервера для использования вызывающим процессом.</span><span class="sxs-lookup"><span data-stu-id="d6598-113">Initializes the HTTP Server API for use by the calling process.</span></span>                                                                   |
| [<span data-ttu-id="d6598-114">**хттппрепареурл**</span><span class="sxs-lookup"><span data-stu-id="d6598-114">**HttpPrepareUrl**</span></span>](/windows/desktop/api/Http/nf-http-httpprepareurl)             | <span data-ttu-id="d6598-115">Анализирует, анализирует и нормализует Ненормализованный URL-адрес в Юникоде или Punycode, поэтому он является надежным и допустимым для использования в других функциях HTTP.</span><span class="sxs-lookup"><span data-stu-id="d6598-115">Parses, analyzes, and normalizes a non-normalized Unicode or punycode URL so it is safe and valid to use in other HTTP functions.</span></span> |
| [<span data-ttu-id="d6598-116">**хттптерминате**</span><span class="sxs-lookup"><span data-stu-id="d6598-116">**HttpTerminate**</span></span>](/windows/desktop/api/Http/nf-http-httpterminate)               | <span data-ttu-id="d6598-117">Направляет API сервера HTTP для очистки всех ресурсов, связанных с определенным процессом.</span><span class="sxs-lookup"><span data-stu-id="d6598-117">Directs the HTTP Server API to clean up any resources associated with a particular process.</span></span>                                       |



 

## <a name="cache-management"></a><span data-ttu-id="d6598-118">Управление кэшем</span><span class="sxs-lookup"><span data-stu-id="d6598-118">Cache Management</span></span>



| <span data-ttu-id="d6598-119">Функция</span><span class="sxs-lookup"><span data-stu-id="d6598-119">Function</span></span>                                                       | <span data-ttu-id="d6598-120">Описание</span><span class="sxs-lookup"><span data-stu-id="d6598-120">Description</span></span>                                                                                            |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d6598-121">**хттпаддфрагменттокаче**</span><span class="sxs-lookup"><span data-stu-id="d6598-121">**HttpAddFragmentToCache**</span></span>](/windows/desktop/api/Http/nf-http-httpaddfragmenttocache)       | <span data-ttu-id="d6598-122">Кэширует фрагмент данных таким образом, чтобы его можно было использовать для составления динамического ответа без считывания с диска.</span><span class="sxs-lookup"><span data-stu-id="d6598-122">Caches a data fragment so that it can be used to compose a dynamic response without reading from disk.</span></span> |
| [<span data-ttu-id="d6598-123">**хттпфлушреспонсекаче**</span><span class="sxs-lookup"><span data-stu-id="d6598-123">**HttpFlushResponseCache**</span></span>](/windows/desktop/api/Http/nf-http-httpflushresponsecache)       | <span data-ttu-id="d6598-124">Удаляет указанные кэшированные фрагменты из кэша HTTP.</span><span class="sxs-lookup"><span data-stu-id="d6598-124">Removes specified cached fragments from the HTTP cache.</span></span>                                                |
| [<span data-ttu-id="d6598-125">**хттпреадфрагментфромкаче**</span><span class="sxs-lookup"><span data-stu-id="d6598-125">**HttpReadFragmentFromCache**</span></span>](/windows/desktop/api/Http/nf-http-httpreadfragmentfromcache) | <span data-ttu-id="d6598-126">Извлекает указанный кэшированный фрагмент ответа.</span><span class="sxs-lookup"><span data-stu-id="d6598-126">Retrieves a specified cached response fragment.</span></span>                                                        |



 

## <a name="configuration"></a><span data-ttu-id="d6598-127">Конфигурация</span><span class="sxs-lookup"><span data-stu-id="d6598-127">Configuration</span></span>



| <span data-ttu-id="d6598-128">Функция</span><span class="sxs-lookup"><span data-stu-id="d6598-128">Function</span></span>                                                                 | <span data-ttu-id="d6598-129">Описание</span><span class="sxs-lookup"><span data-stu-id="d6598-129">Description</span></span>                                                       |
|--------------------------------------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="d6598-130">**хттпделетесервицеконфигуратион**</span><span class="sxs-lookup"><span data-stu-id="d6598-130">**HttpDeleteServiceConfiguration**</span></span>](/windows/desktop/api/Http/nf-http-httpdeleteserviceconfiguration) | <span data-ttu-id="d6598-131">Удаляет указанные сведения из хранилища конфигураций HTTP.</span><span class="sxs-lookup"><span data-stu-id="d6598-131">Deletes specified information from the HTTP configuration store.</span></span>  |
| [<span data-ttu-id="d6598-132">**хттпкуерисервицеконфигуратион**</span><span class="sxs-lookup"><span data-stu-id="d6598-132">**HttpQueryServiceConfiguration**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryserviceconfiguration)   | <span data-ttu-id="d6598-133">Запрашивает в хранилище конфигурации HTTP указанные сведения.</span><span class="sxs-lookup"><span data-stu-id="d6598-133">Queries the HTTP configuration store for specified information.</span></span>   |
| [<span data-ttu-id="d6598-134">**хттпсетсервицеконфигуратион**</span><span class="sxs-lookup"><span data-stu-id="d6598-134">**HttpSetServiceConfiguration**</span></span>](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration)       | <span data-ttu-id="d6598-135">Задает указанные значения в хранилище конфигурации API HTTP-сервера.</span><span class="sxs-lookup"><span data-stu-id="d6598-135">Sets specified values in the HTTP Server API configuration store.</span></span> |



 

## <a name="input-and-output"></a><span data-ttu-id="d6598-136">Ввод и вывод</span><span class="sxs-lookup"><span data-stu-id="d6598-136">Input and Output</span></span>



| <span data-ttu-id="d6598-137">Функция</span><span class="sxs-lookup"><span data-stu-id="d6598-137">Function</span></span>                                                             | <span data-ttu-id="d6598-138">Описание</span><span class="sxs-lookup"><span data-stu-id="d6598-138">Description</span></span>                                                    |
|----------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="d6598-139">**хттпрецеивехттпрекуест**</span><span class="sxs-lookup"><span data-stu-id="d6598-139">**HttpReceiveHttpRequest**</span></span>](/windows/desktop/api/Http/nf-http-httpreceivehttprequest)             | <span data-ttu-id="d6598-140">Получает HTTP-запрос из указанной очереди запросов.</span><span class="sxs-lookup"><span data-stu-id="d6598-140">Retrieves an HTTP request from a specified request queue.</span></span>      |
| [<span data-ttu-id="d6598-141">**хттпрецеиверекуестентитибоди**</span><span class="sxs-lookup"><span data-stu-id="d6598-141">**HttpReceiveRequestEntityBody**</span></span>](/windows/desktop/api/Http/nf-http-httpreceiverequestentitybody) | <span data-ttu-id="d6598-142">Извлекает данные о тексте сущности для конкретного HTTP-запроса.</span><span class="sxs-lookup"><span data-stu-id="d6598-142">Retrieves entity-body data of a particular HTTP request.</span></span>       |
| [<span data-ttu-id="d6598-143">**хттпсендхттпреспонсе**</span><span class="sxs-lookup"><span data-stu-id="d6598-143">**HttpSendHttpResponse**</span></span>](/windows/desktop/api/Http/nf-http-httpsendhttpresponse)                 | <span data-ttu-id="d6598-144">Отправляет HTTP-ответ для конкретного HTTP-запроса.</span><span class="sxs-lookup"><span data-stu-id="d6598-144">Sends an HTTP response for a particular HTTP request.</span></span>          |
| [<span data-ttu-id="d6598-145">**хттпсендреспонсинтитибоди**</span><span class="sxs-lookup"><span data-stu-id="d6598-145">**HttpSendResponseEntityBody**</span></span>](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody)     | <span data-ttu-id="d6598-146">Отправляет данные о тексте сущности в ответе HTTP.</span><span class="sxs-lookup"><span data-stu-id="d6598-146">Sends entity-body data of an HTTP response.</span></span>                    |
| [<span data-ttu-id="d6598-147">**хттпваитфордисконнект**</span><span class="sxs-lookup"><span data-stu-id="d6598-147">**HttpWaitForDisconnect**</span></span>](/windows/desktop/api/Http/nf-http-httpwaitfordisconnect)               | <span data-ttu-id="d6598-148">Уведомляет приложение, когда HTTP-клиент отключен.</span><span class="sxs-lookup"><span data-stu-id="d6598-148">Notifies the application when an HTTP client has disconnected.</span></span> |



 

## <a name="ssl"></a><span data-ttu-id="d6598-149">SSL</span><span class="sxs-lookup"><span data-stu-id="d6598-149">SSL</span></span>



| <span data-ttu-id="d6598-150">Функция</span><span class="sxs-lookup"><span data-stu-id="d6598-150">Function</span></span>                                                             | <span data-ttu-id="d6598-151">Описание</span><span class="sxs-lookup"><span data-stu-id="d6598-151">Description</span></span>                                             |
|----------------------------------------------------------------------|---------------------------------------------------------|
| [<span data-ttu-id="d6598-152">**хттпрецеивеклиентцертификате**</span><span class="sxs-lookup"><span data-stu-id="d6598-152">**HttpReceiveClientCertificate**</span></span>](/windows/desktop/api/Http/nf-http-httpreceiveclientcertificate) | <span data-ttu-id="d6598-153">Получает сертификат клиента для SSL-соединения.</span><span class="sxs-lookup"><span data-stu-id="d6598-153">Retrieves the client certificate for an SSL connection.</span></span> |



 

## <a name="url-registration"></a><span data-ttu-id="d6598-154">Регистрация URL-адреса</span><span class="sxs-lookup"><span data-stu-id="d6598-154">URL Registration</span></span>



| <span data-ttu-id="d6598-155">Функция</span><span class="sxs-lookup"><span data-stu-id="d6598-155">Function</span></span>                               | <span data-ttu-id="d6598-156">Описание</span><span class="sxs-lookup"><span data-stu-id="d6598-156">Description</span></span>                                                                                     |
|----------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d6598-157">**хттпаддурл**</span><span class="sxs-lookup"><span data-stu-id="d6598-157">**HttpAddUrl**</span></span>](/windows/desktop/api/Http/nf-http-httpaddurl)       | <span data-ttu-id="d6598-158">Регистрирует URL-адрес, чтобы HTTP-запросы для него направлялись в указанную очередь запросов.</span><span class="sxs-lookup"><span data-stu-id="d6598-158">Registers a URL so that HTTP requests for it are routed to a specified request queue.</span></span>           |
| [<span data-ttu-id="d6598-159">**хттпремовеурл**</span><span class="sxs-lookup"><span data-stu-id="d6598-159">**HttpRemoveUrl**</span></span>](/windows/desktop/api/Http/nf-http-httpremoveurl) | <span data-ttu-id="d6598-160">Отменяет регистрацию указанного URL-адреса, чтобы запросы для него больше не направлялись в указанную очередь.</span><span class="sxs-lookup"><span data-stu-id="d6598-160">Unregisters a specified URL, so that requests for it are no longer routed to a specified queue.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="d6598-161">См. также</span><span class="sxs-lookup"><span data-stu-id="d6598-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6598-162">Структуры API HTTP-сервера версии 1,0</span><span class="sxs-lookup"><span data-stu-id="d6598-162">HTTP Server API Version 1.0 Structures</span></span>](http-server-api-version-1-0-structures.md)
</dt> </dl>

 

 




