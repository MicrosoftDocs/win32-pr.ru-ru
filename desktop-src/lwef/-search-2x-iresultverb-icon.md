---
title: Свойство Icon Иресултверб (Вдсшаредидл. h)
description: Это свойство возвращает указатель на маркер необязательного значка, связанного с командой.
ms.assetid: 19de0e36-b453-48a4-8ac0-f26432e088ae
keywords:
- свойство Icon устаревшие функции Windows среды
- свойство Icon устаревшие функции Windows среды, интерфейс иресултверб
- интерфейс иресултверб устаревшие функции среды Windows, свойство Icon
topic_type:
- apiref
api_name:
- IResultVerb.Icon
- IResultVerb.get_Icon
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef3715aacb0fd2f4bb0f47424d239e3d4b9717d83471906de8d1b2637fab472a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117694732"
---
# <a name="iresultverbicon-property"></a>Свойство Иресултверб:: Icon

> [!NOTE]
> Windows настольный поиск 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003. в более поздних выпусках используйте вместо этого [API Windows поиска](../search/-search-reference-entry-page.md) . 

Это свойство возвращает указатель на маркер необязательного значка, связанного с командой.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_Icon(
  [out, retval] SHANDLE_PTR *hicon
);
```



## <a name="property-value"></a>Значение свойства

Хикон — это указатель на маркер необязательного значка ассокуатед с командой.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP с пакетом обновления 2 (SP2) \[ только классические приложения\]<br/>                                      |
| Минимальная версия сервера<br/> | Windows Только для настольных приложений сервера 2003 с пакетом обновления 1 \[\]<br/>                             |
| Распространяемые компоненты<br/>          | Windows Поиск на рабочем столе (WDS) 2.6.5<br/>                                             |
| Заголовок<br/>                   | <dl> <dt>Вдсшаредидл. h</dt> </dl> |



 

 





