---
title: Свойство UID Иресултпроперти (Вдсшаредидл. h)
description: Уникальный идентификатор свойства.
ms.assetid: b5cee5b3-78b4-4d2a-b442-f6624497ef71
keywords:
- Свойства UID устаревшие функции среды Windows
- Свойство UID устаревшие компоненты среды Windows, интерфейс Иресултпроперти
- Интерфейс Иресултпроперти устаревшие функции среды Windows, свойство UID
topic_type:
- apiref
api_name:
- IResultProperty.UID
- IResultProperty.get_UID
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a08921e366cca2be40a8a79fe43d7a15cec54f2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071479"
---
# <a name="iresultpropertyuid-property"></a>Свойство Иресултпроперти:: UID

> [!NOTE]
> Windows Desktop Search 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003. В более поздних выпусках используйте [API поиска Windows](../search/-search-reference-entry-page.md) . 

Уникальный идентификатор свойства.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_UID(
  [out, retval] long *uid
);
```



## <a name="property-value"></a>Значение свойства

Возвращает указатель на уникальный идентификатор свойства.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для настольных приложений Windows XP с пакетом обновления 2 \[\]<br/>                                      |
| Минимальная версия сервера<br/> | Только для настольных приложений Windows Server 2003 с пакетом обновления 1 \[\]<br/>                             |
| Распространяемые компоненты<br/>          | Windows Desktop Search (WDS) версии 2.6.5<br/>                                             |
| Header<br/>                   | <dl> <dt>Вдсшаредидл. h</dt> </dl> |



 

 





