---
title: Свойство Ипропертифилтерколлектион-ITem (Вдсшаредидл. h)
description: Возвращает конкретный фильтр в коллекции.
ms.assetid: 72a35d98-b2d8-4dfb-84a7-365a3778fc85
keywords:
- свойства элемента Windows устаревшие функции среды
- свойство item Windows устаревшие функции среды, интерфейс ипропертифилтерколлектион
- устаревшие функции среды Windows интерфейса ипропертифилтерколлектион, свойство dataitem
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
ms.openlocfilehash: 7436e1fe10c26621f3cf4480be7db9710f80906bea18084a2e775e563db4dd8a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119451086"
---
# <a name="ipropertyfiltercollectiongetitem-property"></a>Свойство Ипропертифилтерколлектион:: ITem

> [!NOTE]
> Windows настольный поиск 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003. в более поздних выпусках используйте вместо этого [API Windows поиска](../search/-search-reference-entry-page.md) . 

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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP с пакетом обновления 2 (SP2) \[ только классические приложения\]<br/>                                      |
| Минимальная версия сервера<br/> | Windows Только для настольных приложений сервера 2003 с пакетом обновления 1 \[\]<br/>                             |
| Распространяемые компоненты<br/>          | Windows Поиск на рабочем столе (WDS) 2.6.5<br/>                                             |
| Header<br/>                   | <dl> <dt>Вдсшаредидл. h</dt> </dl> |



 

 





