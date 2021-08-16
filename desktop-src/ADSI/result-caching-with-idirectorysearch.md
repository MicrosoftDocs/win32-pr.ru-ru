---
title: Кэширование результатов с помощью IDirectorySearch
description: Параметр ADS \_ сеарчпреф \_ кэша \_ результатов кэширует результирующий набор на клиенте.
ms.assetid: bb286879-7d84-4085-88e1-600c848b8af8
ms.tgt_platform: multiple
keywords:
- Кэширование результатов с помощью IDirectorySearch ADSI
- ADSI, поиск, IDirectorySearch, другие параметры поиска, кэширование результатов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4febc2f02e03759861978e062ee972d8e90df27b996c8161d6163e764fefe9a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117838860"
---
# <a name="result-caching-with-idirectorysearch"></a>Кэширование результатов с помощью IDirectorySearch

Параметр **ADS \_ сеарчпреф \_ кэша \_ результатов** кэширует результирующий набор на клиенте. Кэширование результатов позволяет приложению хранить полученный результирующий набор и повторно проходить извлеченные строки. Он также обеспечивает поддержку курсора, где методы [**IDirectorySearch:: GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) и [**IDirectorySearch:: жетпревиаусров**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getpreviousrow) можно использовать для перемещения результирующего набора вверх и вниз.

По умолчанию кэширование результатов отключено. Кэширование результатов должно быть включено, если выполняется одно из следующих условий.

-   Значение, если один и тот же результирующий набор необходимо перечислить несколько раз без повторного выполнения поиска на сервере.
-   Если выполнение поиска занимает много ресурсов на сервере (медленное подключение, большой результирующий набор или сложный запрос).
-   Значение, если требуется поддержка курсора.

Отключите кэширование, если приложение должно уменьшить требования к памяти для кэширования большого результирующего набора на клиенте.

Кэширование результатов увеличивает требования к памяти на клиенте, поэтому кэширование результатов должно быть отключено, если это является проблемой.

Чтобы включить кэширование результатов, установите параметр поиска **\_ \_ \_ результатов кэша Сеарчпреф** с логическим значением **адстипе \_** , равным **true** , в массиве [**\_ \_ сведений об ADS сеарчпреф**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) , переданном в метод [**IDirectorySearch:: сетсеарчпреференце**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .

В следующем примере кода показано, как включить кэширование результатов.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_CACHE_RESULTS;
SearchPref.vValue.dwType = ADSTYPE_BOOLEAN;
SearchPref.vValue.Boolean = TRUE;
```



 

 




