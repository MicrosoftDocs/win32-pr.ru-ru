---
title: Указание других параметров поиска с помощью IDirectorySearch
description: Интерфейс IDirectorySearch обеспечивает дополнительный контроль над выполнением поиска с помощью параметров поиска.
ms.assetid: 91b7ba90-99b3-4137-8e4e-8d0ccfb0ec13
ms.tgt_platform: multiple
keywords:
- Указание других параметров поиска с помощью IDirectorySearch ADSI
- ADSI, поиск, IDirectorySearch, другие параметры поиска
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67105d9716934c8c7d1d56193ca0cdfde5f6a4bc4c32605420513dc62700d8b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118178769"
---
# <a name="specifying-other-search-options-with-idirectorysearch"></a>Указание других параметров поиска с помощью IDirectorySearch

Интерфейс [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) обеспечивает дополнительный контроль над выполнением поиска с помощью параметров поиска. Эти параметры поиска задаются путем заполнения массива структур [**\_ \_ сведений сеарчпреф ADS**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) и вызова метода [**IDirectorySearch:: сетсеарчпреференце**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) . Дополнительные сведения см. в следующих разделах:

-   [Использование метода Сетсеарчпреференце](using-the-setsearchpreference-method.md)
-   [Синхронный и асинхронный поиск с помощью IDirectorySearch](synchronous-and-asynchronous-searches-with-idirectorysearch.md)
-   [Подкачка с помощью IDirectorySearch](paging-with-idirectorysearch.md)
-   [Кэширование результатов с помощью IDirectorySearch](result-caching-with-idirectorysearch.md)
-   [Выполнение запроса к области атрибута](performing-an-attribute-scoped-query.md)
-   [Сортировка результатов поиска с помощью IDirectorySearch](sorting-the-search-results-with-idirectorysearch.md)
-   [Отслеживание ссылок с помощью IDirectorySearch](referral-chasing-with-idirectorysearch.md)
-   [Ограничение размера с IDirectorySearch](size-limit-with-idirectorysearch.md)
-   [Ограничение времени сервера на IDirectorySearch](server-time-limit-with-idirectorysearch.md)
-   [Ограничение времени клиента с помощью IDirectorySearch](client-time-limit-with-idirectorysearch.md)
-   [Возвращение только имен атрибутов с помощью IDirectorySearch](returning-only-attribute-names-with-idirectorysearch.md)

 

 




