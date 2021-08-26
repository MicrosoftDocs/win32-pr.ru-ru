---
title: Изменение атрибутов с помощью ADSI
description: Чтобы изменить значения атрибутов, ADSI предоставляет методы IADs. Where и IADs. Путекс. Эти методы изменяют данные в кэше на стороне клиента. Для фиксации изменений в каталоге необходимо вызвать метод IADs. Сетинфо.
ms.assetid: cbb5c313-3b9d-4943-bd16-6e4489abe804
ms.tgt_platform: multiple
keywords:
- Изменение атрибутов с помощью ADSI
- Атрибуты ADSI, изменение
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef82d6a3d4c486fcd1fca1f5cba7ae62f57e66e713ed84551a5a9372cdc86683
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079964"
---
# <a name="modifying-attributes-with-adsi"></a>Изменение атрибутов с помощью ADSI

Чтобы изменить значения атрибутов, ADSI предоставляет методы [**iAds.**](/windows/desktop/api/Iads/nf-iads-iads-put) WHERE и [**iAds. путекс**](/windows/desktop/api/Iads/nf-iads-iads-putex) . Эти методы изменяют данные в кэше на стороне клиента. Для фиксации изменений в каталоге необходимо вызвать метод [**iAds. сетинфо**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) .

> [!Note]  
> Если изменение нескольких атрибутов фиксируется в одном вызове [**iAds. сетинфо**](/windows/desktop/api/Iads/nf-iads-iads-setinfo), если какой-либо отдельный атрибут не может быть изменен, ни один из атрибутов не будет изменен. Например, если изменить атрибуты [**SN**](/windows/desktop/ADSchema/a-sn) и [**givenName**](/windows/desktop/ADSchema/a-givenname) и очистить атрибут [**telephoneNumber**](/windows/desktop/ADSchema/a-telephonenumber) объекта пользователя без последующих вызовов метода **сетинфо** , изменения будут введены при вызове **сетинфо**. Если одно или несколько изменений не разрешены и, следовательно, не могут быть выполнены, то никакие коллективные изменения, внесенные в атрибуты, не будут введены во время вызова **сетинфо**.

 

Метод [**iAds. помещаем**](/windows/desktop/api/Iads/nf-iads-iads-put) принимает имя атрибута и параметр Variant. Используйте этот метод, чтобы задать атрибуты, которые содержат как одно, так и несколько значений.

Метод [**iAds. путекс**](/windows/desktop/api/Iads/nf-iads-iads-putex) предоставляет контроль над операциями с многозначными атрибутами. Можно добавлять, удалять, обновлять и очищать существующие значения. Метод **iAds. путекс** всегда принимает массив вариантов значений атрибутов. Однако этот метод можно использовать для задания одного и того же значения атрибута.

Метод [**iAds. путекс**](/windows/desktop/api/Iads/nf-iads-iads-putex) использует операции, указанные в перечислении [**\_ \_ \_ enum операции свойства ADS**](/windows/win32/api/iads/ne-iads-ads_property_operation_enum) .

 

 