---
title: Свойство UID Иресултпроперти (Вдсшаредидл. h)
description: Уникальный идентификатор свойства.
ms.assetid: b5cee5b3-78b4-4d2a-b442-f6624497ef71
keywords:
- свойства UID, устаревшие Windows функции среды
- свойства UID, устаревшие Windows функции среды, интерфейс иресултпроперти
- интерфейс иресултпроперти устаревшие функции среды Windows, свойство UID
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
ms.openlocfilehash: d413a81d6b18091d2e21b4572f5f8e01693829c17942d3e395e2c03a71d467d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118754727"
---
# <a name="iresultpropertyuid-property"></a>Свойство Иресултпроперти:: UID

> [!NOTE]
> Windows настольный поиск 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003. в более поздних выпусках используйте вместо этого [API Windows поиска](../search/-search-reference-entry-page.md) . 

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
| Минимальная версия клиента<br/> | Windows XP с пакетом обновления 2 (SP2) \[ только классические приложения\]<br/>                                      |
| Минимальная версия сервера<br/> | Windows Только для настольных приложений сервера 2003 с пакетом обновления 1 \[\]<br/>                             |
| Распространяемые компоненты<br/>          | Windows Поиск на рабочем столе (WDS) 2.6.5<br/>                                             |
| Header<br/>                   | <dl> <dt>Вдсшаредидл. h</dt> </dl> |



 

 





