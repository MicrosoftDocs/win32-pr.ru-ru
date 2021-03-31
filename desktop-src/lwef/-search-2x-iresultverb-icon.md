---
title: Свойство Icon Иресултверб (Вдсшаредидл. h)
description: Это свойство возвращает указатель на маркер необязательного значка, связанного с командой.
ms.assetid: 19de0e36-b453-48a4-8ac0-f26432e088ae
keywords:
- Свойство Icon устаревшие функции среды Windows
- Свойство Icon устаревшие функции среды Windows, интерфейс Иресултверб
- Интерфейс Иресултверб устаревшие функции среды Windows, свойство Icon
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
ms.openlocfilehash: f2babd2a9e45f1d038d5f7ce567eeaaf37e1f29f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491559"
---
# <a name="iresultverbicon-property"></a>Свойство Иресултверб:: Icon

> [!NOTE]
> Windows Desktop Search 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003. В более поздних выпусках используйте [API поиска Windows](../search/-search-reference-entry-page.md) . 

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
| Минимальная версия клиента<br/> | Только для настольных приложений Windows XP с пакетом обновления 2 \[\]<br/>                                      |
| Минимальная версия сервера<br/> | Только для настольных приложений Windows Server 2003 с пакетом обновления 1 \[\]<br/>                             |
| Распространяемые компоненты<br/>          | Windows Desktop Search (WDS) версии 2.6.5<br/>                                             |
| Header<br/>                   | <dl> <dt>Вдсшаредидл. h</dt> </dl> |



 

 





