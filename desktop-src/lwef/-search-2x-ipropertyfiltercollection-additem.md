---
title: Свойство AddItem Ипропертифилтерколлектион (Вдсшаредидл. h)
description: Добавляет новый фильтр в коллекцию.
ms.assetid: 01078e7a-811a-4dfb-b122-4801f39413d8
keywords:
- Свойства AddItem устаревшие функции среды Windows
- Свойство AddItem устаревшие функции среды Windows, интерфейс Ипропертифилтерколлектион
- Интерфейс Ипропертифилтерколлектион устаревшие функции среды Windows, свойство AddItem
topic_type:
- apiref
api_name:
- IPropertyFilterCollection.AddItem
- IPropertyFilterCollection.get_AddItem
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b199f0e696f75fb5549b274ac888989f7a723b48
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071480"
---
# <a name="ipropertyfiltercollectionadditem-property"></a>Свойство Ипропертифилтерколлектион:: AddItem

> [!NOTE]
> Windows Desktop Search 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003. В более поздних выпусках используйте [API поиска Windows](../search/-search-reference-entry-page.md) . 

Добавляет новый фильтр в коллекцию.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_AddItem(
  [out, retval] IPropertyFilter **filter
);
```



## <a name="property-value"></a>Значение свойства

Возвращает указатель на адрес для нового фильтра.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для настольных приложений Windows XP с пакетом обновления 2 \[\]<br/>                                      |
| Минимальная версия сервера<br/> | Только для настольных приложений Windows Server 2003 с пакетом обновления 1 \[\]<br/>                             |
| Распространяемые компоненты<br/>          | Windows Desktop Search (WDS) версии 2.6.5<br/>                                             |
| Header<br/>                   | <dl> <dt>Вдсшаредидл. h</dt> </dl> |



 

 





