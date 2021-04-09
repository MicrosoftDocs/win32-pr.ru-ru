---
title: Динамическое создание документа ServiceInfo
description: Динамическое создание документа ServiceInfo
ms.assetid: 96937b04-f705-49f6-8ddf-25c98a51dc9a
keywords:
- Интернет-магазины проигрывателя Windows Media, создание документа ServiceInfo
- Интернет-магазины, создание документа ServiceInfo
- Тип 1 Интернет-магазины, создание документа ServiceInfo
- Тип 2 Интернет-магазинов, создание документа ServiceInfo
- Интернет-магазины проигрывателя Windows Media, динамическое создание документа ServiceInfo
- Интернет-магазины, динамическое создание документа ServiceInfo
- Введите 1 Интернет-магазины, динамически создавая документ ServiceInfo
- Тип 2 Интернет-магазинов, динамическое создание документа ServiceInfo
- Интернет-магазины проигрывателя Windows Media, документ ServiceInfo
- Интернет-магазины, документ ServiceInfo
- Тип 1 Интернет-магазины, документ ServiceInfo
- Тип 2 Интернет-магазинов, документ ServiceInfo
- Динамическое создание документа ServiceInfo
- Создание документа ServiceInfo
- Документ ServiceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90159e72046536cf6b69521586a0640935478eb1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986187"
---
# <a name="creating-the-serviceinfo-document-dynamically"></a><span data-ttu-id="e70d0-118">Динамическое создание документа ServiceInfo</span><span class="sxs-lookup"><span data-stu-id="e70d0-118">Creating the ServiceInfo Document Dynamically</span></span>

<span data-ttu-id="e70d0-119">Для создания документа ServiceInfo можно использовать технологию ASP.</span><span class="sxs-lookup"><span data-stu-id="e70d0-119">You can use ASP to create your ServiceInfo document.</span></span> <span data-ttu-id="e70d0-120">Это обеспечивает большую гибкость в Интернет-магазине, используя следующие методы:</span><span class="sxs-lookup"><span data-stu-id="e70d0-120">This can give you greater flexibility in your online store by using the following techniques:</span></span>

-   <span data-ttu-id="e70d0-121">Динамическое создание имени узла для URL-адресов.</span><span class="sxs-lookup"><span data-stu-id="e70d0-121">Dynamically generating the host name for URLs.</span></span>
-   <span data-ttu-id="e70d0-122">Изменение URL-адресов для локализации на основе параметров языкового стандарта и GeoId.</span><span class="sxs-lookup"><span data-stu-id="e70d0-122">Changing URLs for localization based on locale and geoid parameters.</span></span>
-   <span data-ttu-id="e70d0-123">Динамическое добавление параметров строки запроса из URL-адреса ServiceInfo к другим URL-адресам, таким как URL-адрес страницы перехода.</span><span class="sxs-lookup"><span data-stu-id="e70d0-123">Dynamically appending query string parameters from the ServiceInfo URL to other URLs, such as the navigate page URL.</span></span>

<span data-ttu-id="e70d0-124">В следующем примере кода показана простая страница ASP, которая динамически создает документ ServiceInfo:</span><span class="sxs-lookup"><span data-stu-id="e70d0-124">The following example code shows a simple ASP page that dynamically creates a ServiceInfo document:</span></span>


```C++
<%
    Dim sHost
    Dim sLocale

    sHost = Request.ServerVariables("HTTP_HOST")
    sLocale = Request.QueryString("locale")
%>

<?xml version="1.0" encoding="utf-8"?>
<ServiceInfo Version="1.00" Key="MyCommerceService">
    <FriendlyName>My Online Store</FriendlyName>
    <ServiceTask1
        URL = "https://<%= sHost %>/service/html/Music.asp">
    </ServiceTask1>
    <ServiceTask2
        URL = "https://<%= sHost %>/service/html/Video.asp">
    </ServiceTask2>
    <ServiceTask3
        URL = "https://<%= sHost %>/service/html/Radio.asp">
    </ServiceTask3>
    <Navigate
        BaseURL = "https://<%= sHost %>/service/html/navigate.asp?myloc<%= sLocale %>">
    </Navigate>
</ServiceInfo>
```



<span data-ttu-id="e70d0-125">В предыдущем примере кода используется ASP для получения имени узла с веб-сервера и динамического создания URL-адресов в документе.</span><span class="sxs-lookup"><span data-stu-id="e70d0-125">The preceding example code uses ASP to retrieve the host name from the web server and dynamically create the URLs in the document.</span></span> <span data-ttu-id="e70d0-126">Код также извлекает параметр строки запроса *локали* из запроса serviceInfo и добавляет его к URL-адресу страницы перехода.</span><span class="sxs-lookup"><span data-stu-id="e70d0-126">The code also retrieves the *locale* query string parameter from the ServiceInfo request and appends it to the URL for the navigate page.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e70d0-127">См. также</span><span class="sxs-lookup"><span data-stu-id="e70d0-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e70d0-128">**Сведения, общие для типа 1 и 2 Интернет-магазинов**</span><span class="sxs-lookup"><span data-stu-id="e70d0-128">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="e70d0-129">**Навигация для Интернет-магазинов типа 2**</span><span class="sxs-lookup"><span data-stu-id="e70d0-129">**Navigation for Type 2 Online Stores**</span></span>](navigation-for-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="e70d0-130">**Документ ServiceInfo для Интернет-магазина типа 1**</span><span class="sxs-lookup"><span data-stu-id="e70d0-130">**ServiceInfo Document for a Type 1 Online Store**</span></span>](serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="e70d0-131">**Документ ServiceInfo для Интернет-магазина типа 2**</span><span class="sxs-lookup"><span data-stu-id="e70d0-131">**ServiceInfo Document for a Type 2 Online Store**</span></span>](serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="e70d0-132">**Документ ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="e70d0-132">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 




