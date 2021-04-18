---
title: Свойство DisplayName Иресулттипе (Вдсшаредидл. h)
description: Локализованное отображаемое имя типа
ms.assetid: 21695ba3-aa6d-419b-961a-0643caa5ea1f
keywords:
- Свойства DisplayName устаревшие функции среды Windows
- Свойства DisplayName устаревшие компоненты среды Windows, интерфейс Иресулттипе
- Интерфейс Иресулттипе устаревшие функции среды Windows, свойство DisplayName
topic_type:
- apiref
api_name:
- IResultType.DisplayName
- IResultType.get_DisplayName
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94080a2b5c6121bbaa9b611a7d55c2d5aaeed5e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105701037"
---
# <a name="iresulttypedisplayname-property"></a>Иресулттипе: свойство Исплайнаме:D

> [!NOTE]
> Windows Desktop Search 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003. В более поздних выпусках используйте [API поиска Windows](../search/-search-reference-entry-page.md) . 

Локализованное отображаемое имя типа:

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_DisplayName(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a>Значение свойства

Возвращает адрес локализованного отображаемого имени для типа.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для настольных приложений Windows XP с пакетом обновления 2 \[\]<br/>                                      |
| Минимальная версия сервера<br/> | Только для настольных приложений Windows Server 2003 с пакетом обновления 1 \[\]<br/>                             |
| Распространяемые компоненты<br/>          | Windows Desktop Search (WDS) версии 2.6.5<br/>                                             |
| Header<br/>                   | <dl> <dt>Вдсшаредидл. h</dt> </dl> |



 

 





