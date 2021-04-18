---
title: Возвращение только имен атрибутов с помощью IDirectorySearch
description: Чтобы определить, какой тип данных доступен для конкретного объекта, можно выполнить поиск.
ms.assetid: 47e78b79-2063-420b-aa41-f4f0c35f87ea
ms.tgt_platform: multiple
keywords:
- Возвращение только имен атрибутов с помощью IDirectorySearch ADSI
- ADSI, поиск, IDirectorySearch, другие параметры поиска, возвращающие только имена атрибутов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 055acbb3fe19969ce95ea77a633e20b195c0257d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105654107"
---
# <a name="returning-only-attribute-names-with-idirectorysearch"></a>Возвращение только имен атрибутов с помощью IDirectorySearch

Чтобы определить, какой тип данных доступен для конкретного объекта, можно выполнить поиск. В этом случае вы заинтересованы только в именах атрибутов, а не на значениях атрибутов объекта. Параметр **ADS \_ сеарчпреф \_ аттрибтипес \_ только** указывает, что сервер возвращает только имена атрибутов, а не значения атрибутов. Однако результирующий набор включает только те атрибуты, которые имеют присвоенные значения. Например, рассмотрим объект со следующими атрибутами:

``` syntax
name = Jeff
sn = Smith
department = Empty
phone = 206-555-0111
```

Если установлен параметр " **ADS \_ сеарчпреф \_ аттрибтипес \_** ", результирующий набор включает:

``` syntax
name
sn
department
phone
```

Значение по умолчанию — для возвращаемых значений и имен атрибутов.

Чтобы получить только имена атрибутов, установите параметр **ADS \_ сеарчпреф \_ аттрибтипес \_ только** с **\_ логическим значением адстипе** , равным **true** , в массиве [**\_ \_ сведений ADS сеарчпреф**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) , переданном в метод [**IDirectorySearch:: сетсеарчпреференце**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .

В следующем примере кода показано, как получить только имена атрибутов.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_ATTRIBTYPES_ONLY;
SearchPref.vValue.dwType = ADSTYPE_BOOLEAN;
SearchPref.vValue.Boolean = TRUE;
```



Дополнительные сведения и пример кода, демонстрирующий использование параметра поиска **ADS \_ сеарчпреф \_ аттрибтипес \_ только** , см. в разделе [пример кода для поиска атрибутов](example-code-for-searching-for-attributes.md).

 

 




