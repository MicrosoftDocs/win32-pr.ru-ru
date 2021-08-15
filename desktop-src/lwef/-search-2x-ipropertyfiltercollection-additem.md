---
title: Свойство AddItem Ипропертифилтерколлектион (Вдсшаредидл. h)
description: Добавляет новый фильтр в коллекцию.
ms.assetid: 01078e7a-811a-4dfb-b122-4801f39413d8
keywords:
- свойства функции AddItem прежних версий Windows среды
- свойства AddItem устаревшей Windows среды, интерфейс ипропертифилтерколлектион
- устаревшие функции Windows интерфейсов интерфейса ипропертифилтерколлектион, свойство AddItem
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
ms.openlocfilehash: aeafec95549fefa244dff6ff44ad9110150ae1b410e38b423a0a31f09cf54194
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118755451"
---
# <a name="ipropertyfiltercollectionadditem-property"></a>Свойство Ипропертифилтерколлектион:: AddItem

> [!NOTE]
> Windows настольный поиск 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003. в более поздних выпусках используйте вместо этого [API Windows поиска](../search/-search-reference-entry-page.md) . 

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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP с пакетом обновления 2 (SP2) \[ только классические приложения\]<br/>                                      |
| Минимальная версия сервера<br/> | Windows Только для настольных приложений сервера 2003 с пакетом обновления 1 \[\]<br/>                             |
| Распространяемые компоненты<br/>          | Windows Поиск на рабочем столе (WDS) 2.6.5<br/>                                             |
| Header<br/>                   | <dl> <dt>Вдсшаредидл. h</dt> </dl> |



 

 





