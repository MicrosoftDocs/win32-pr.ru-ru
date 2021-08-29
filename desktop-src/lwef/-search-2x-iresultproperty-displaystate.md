---
title: Свойство Дисплайстате Иресултпроперти (Вдсшаредидл. h)
description: Висабилити свойства.
ms.assetid: 4fdf6cdb-30bd-4582-a573-a1cc9f4052e6
keywords:
- свойства дисплайстате устаревшей среды Windows
- свойства дисплайстате устаревшей среды Windows, интерфейс иресултпроперти
- интерфейс иресултпроперти устаревшие функции среды Windows, свойство дисплайстате
topic_type:
- apiref
api_name:
- IResultProperty.DisplayState
- IResultProperty.get_DisplayState
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6cf4e8e285479f0c1d15d3c846e12786113410198935df5f83056ee89f39792
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118755156"
---
# <a name="iresultpropertydisplaystate-property"></a>Иресултпроперти: свойство Исплайстате:D

> [!NOTE]
> Windows настольный поиск 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003. в более поздних выпусках используйте вместо этого [API Windows поиска](../search/-search-reference-entry-page.md) . 

Висабилити свойства.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_DisplayState(
  [out, retval] PropertyDisplayState *state
);
```



## <a name="property-value"></a>Значение свойства

Возвращает указатель на значение состояния отображения.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP с пакетом обновления 2 (SP2) \[ только классические приложения\]<br/>                                      |
| Минимальная версия сервера<br/> | Windows Только для настольных приложений сервера 2003 с пакетом обновления 1 \[\]<br/>                             |
| Распространяемые компоненты<br/>          | Windows Поиск на рабочем столе (WDS) 2.6.5<br/>                                             |
| Header<br/>                   | <dl> <dt>Вдсшаредидл. h</dt> </dl> |



 

 





