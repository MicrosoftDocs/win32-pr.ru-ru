---
title: Свойство Ипропертифилтерколлектион-ITem (Вдсшаредидл. h)
description: Возвращает конкретный фильтр в коллекции.
ms.assetid: 72a35d98-b2d8-4dfb-84a7-365a3778fc85
keywords:
- Свойство DataItem устаревшие функции среды Windows
- Свойство DataItem устаревшие функции среды Windows, интерфейс Ипропертифилтерколлектион
- Интерфейс Ипропертифилтерколлектион устаревшие функции среды Windows, свойство DataItem
topic_type:
- apiref
api_name:
- IPropertyFilterCollection.GetITem
- IPropertyFilterCollection.get_GetITem
- IPropertyFilterCollection.put_GetITem
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8027bf175efc615c1324f55229c7e307a123c39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988504"
---
# <a name="ipropertyfiltercollectiongetitem-property"></a>Свойство Ипропертифилтерколлектион:: ITem

> [!NOTE]
> Windows Desktop Search 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003. В более поздних выпусках используйте [API поиска Windows](../search/-search-reference-entry-page.md) . 

Возвращает конкретный фильтр в коллекции.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_GetITem(
  [in]          long            index
);

HRESULT get_GetITem(
  [out, retval] IPropertyFilter **filter
);
```



## <a name="property-value"></a>Значение свойства

Задает адрес фильтра.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для настольных приложений Windows XP с пакетом обновления 2 \[\]<br/>                                      |
| Минимальная версия сервера<br/> | Только для настольных приложений Windows Server 2003 с пакетом обновления 1 \[\]<br/>                             |
| Распространяемые компоненты<br/>          | Windows Desktop Search (WDS) версии 2.6.5<br/>                                             |
| Header<br/>                   | <dl> <dt>Вдсшаредидл. h</dt> </dl> |



 

 





