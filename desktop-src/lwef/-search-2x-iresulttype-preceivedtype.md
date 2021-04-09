---
title: Свойство Прецеиведтипе Иресулттипе (Вдсшаредидл. h)
description: Это свойство содержит строку, используемую для задания типа в индексе.
ms.assetid: 26d5f14c-162a-4ded-ac72-875561b8c977
keywords:
- Свойства Прецеиведтипе устаревшие функции среды Windows
- Свойства Прецеиведтипе устаревшие функции среды Windows, интерфейс Иресулттипе
- Интерфейс Иресулттипе устаревшие функции среды Windows, свойство Прецеиведтипе
topic_type:
- apiref
api_name:
- IResultType.PreceivedType
- IResultType.get_PreceivedType
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b058105af254403c3b733f484d7c49a9ac5a0da3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891725"
---
# <a name="iresulttypepreceivedtype-property"></a>Иресулттипе: свойство Рецеиведтипе:P

> [!NOTE]
> Windows Desktop Search 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003. В более поздних выпусках используйте [API поиска Windows](../search/-search-reference-entry-page.md) . 

Это свойство содержит строку, используемую для задания типа в индексе.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_PreceivedType(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a>Значение свойства

Возвращает адрес строки, идентифинт тип в индексе.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для настольных приложений Windows XP с пакетом обновления 2 \[\]<br/>                                      |
| Минимальная версия сервера<br/> | Только для настольных приложений Windows Server 2003 с пакетом обновления 1 \[\]<br/>                             |
| Распространяемые компоненты<br/>          | Windows Desktop Search (WDS) версии 2.6.5<br/>                                             |
| Header<br/>                   | <dl> <dt>Вдсшаредидл. h</dt> </dl> |



 

 





