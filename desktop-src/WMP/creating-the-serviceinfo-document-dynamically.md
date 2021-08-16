---
title: Динамическое создание документа ServiceInfo
description: Динамическое создание документа ServiceInfo
ms.assetid: 96937b04-f705-49f6-8ddf-25c98a51dc9a
keywords:
- проигрыватель Windows Media интернет-магазинов, создание документа ServiceInfo
- Интернет-магазины, создание документа ServiceInfo
- Тип 1 Интернет-магазины, создание документа ServiceInfo
- Тип 2 Интернет-магазинов, создание документа ServiceInfo
- проигрыватель Windows Media интернет-магазинов, динамическое создание документа ServiceInfo
- Интернет-магазины, динамическое создание документа ServiceInfo
- Введите 1 Интернет-магазины, динамически создавая документ ServiceInfo
- Тип 2 Интернет-магазинов, динамическое создание документа ServiceInfo
- проигрыватель Windows Media интернет-магазинов, документ ServiceInfo
- Интернет-магазины, документ ServiceInfo
- Тип 1 Интернет-магазины, документ ServiceInfo
- Тип 2 Интернет-магазинов, документ ServiceInfo
- Динамическое создание документа ServiceInfo
- Создание документа ServiceInfo
- Документ ServiceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3883487d072af57174a1f40f2fcef05d3290917b473a95bf723c34d793c5ba5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118340994"
---
# <a name="creating-the-serviceinfo-document-dynamically"></a>Динамическое создание документа ServiceInfo

Для создания документа ServiceInfo можно использовать технологию ASP. Это обеспечивает большую гибкость в Интернет-магазине, используя следующие методы:

-   Динамическое создание имени узла для URL-адресов.
-   Изменение URL-адресов для локализации на основе параметров языкового стандарта и GeoId.
-   Динамическое добавление параметров строки запроса из URL-адреса ServiceInfo к другим URL-адресам, таким как URL-адрес страницы перехода.

В следующем примере кода показана простая страница ASP, которая динамически создает документ ServiceInfo:


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



В предыдущем примере кода используется ASP для получения имени узла с веб-сервера и динамического создания URL-адресов в документе. Код также извлекает параметр строки запроса *локали* из запроса serviceInfo и добавляет его к URL-адресу страницы перехода.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Сведения, общие для типа 1 и 2 Интернет-магазинов**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Навигация для Интернет-магазинов типа 2**](navigation-for-type-2-online-stores.md)
</dt> <dt>

[**Документ ServiceInfo для Интернет-магазина типа 1**](serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Документ ServiceInfo для Интернет-магазина типа 2**](serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Документ ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 




