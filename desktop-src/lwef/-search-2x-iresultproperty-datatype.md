---
title: Свойство DataType Иресултпроперти (Вдсшаредидл. h)
description: Тип данных Properties.
ms.assetid: 2bf83256-0d69-48f2-aa7d-d34dcba17050
keywords:
- свойства DataType устаревшие Windows функции среды
- свойства DataType устаревшие Windows функции среды, интерфейс иресултпроперти
- интерфейс иресултпроперти устаревшие функции среды Windows, свойство DataType
topic_type:
- apiref
api_name:
- IResultProperty.DataType
- IResultProperty.get_DataType
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f669fdbb01459e99edb0ccc9ba75fed1cbd60ebfe789fdb4393d217239cdc1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118755263"
---
# <a name="iresultpropertydatatype-property"></a>Иресултпроперти: свойство Ататипе:D

> [!NOTE]
> Windows настольный поиск 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003. в более поздних выпусках используйте вместо этого [API Windows поиска](../search/-search-reference-entry-page.md) . 

Тип данных Properties.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_DataType(
  [out, retval] VARTYPE *vt
);
```



## <a name="property-value"></a>Значение свойства

Возвращает указатель на тип данных Properties.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP с пакетом обновления 2 (SP2) \[ только классические приложения\]<br/>                                      |
| Минимальная версия сервера<br/> | Windows Только для настольных приложений сервера 2003 с пакетом обновления 1 \[\]<br/>                             |
| Распространяемые компоненты<br/>          | Windows Поиск на рабочем столе (WDS) 2.6.5<br/>                                             |
| Header<br/>                   | <dl> <dt>Вдсшаредидл. h</dt> </dl> |



 

 





