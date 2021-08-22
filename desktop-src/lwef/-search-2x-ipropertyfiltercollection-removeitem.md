---
title: Свойство RemoveItem Ипропертифилтерколлектион (Вдсшаредидл. h)
description: Удаляет конкретный фильтр в коллекции.
ms.assetid: a8b8a1f7-d47a-45dc-81c9-f01ecf6c1560
keywords:
- свойства RemoveItem устаревшей среды Windows
- свойства RemoveItem устаревшей среды Windows, интерфейс ипропертифилтерколлектион
- интерфейс ипропертифилтерколлектион устаревшие функции среды Windows, свойство RemoveItem
topic_type:
- apiref
api_name:
- IPropertyFilterCollection.RemoveItem
- IPropertyFilterCollection.put_RemoveItem
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54822e95e2ea7d6e10fdd5bbf833adb63b51cb01e8d860ce77f550432b41e926
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118755423"
---
# <a name="ipropertyfiltercollectionremoveitem-property"></a>Свойство Ипропертифилтерколлектион:: RemoveItem

> [!NOTE]
> Windows настольный поиск 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003. в более поздних выпусках используйте вместо этого [API Windows поиска](../search/-search-reference-entry-page.md) . 

Удаляет конкретный фильтр в коллекции.

Это свойство доступно только на запись.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_RemoveItem(
  [in] long index
);
```



## <a name="property-value"></a>Значение свойства

Принимает указатель на индекс удаляемого фильтра.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP с пакетом обновления 2 (SP2) \[ только классические приложения\]<br/>                                      |
| Минимальная версия сервера<br/> | Windows Только для настольных приложений сервера 2003 с пакетом обновления 1 \[\]<br/>                             |
| Распространяемые компоненты<br/>          | Windows Поиск на рабочем столе (WDS) 2.6.5<br/>                                             |
| Header<br/>                   | <dl> <dt>Вдсшаредидл. h</dt> </dl> |



 

 





