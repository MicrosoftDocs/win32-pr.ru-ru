---
title: Свойство DisplayName Иресултверб (Вдсшаредидл. h)
description: Это свойство возвращает указатель на локализованное отображаемое имя для команды.
ms.assetid: f1f4a30e-ecfb-4091-b9cd-312e427d0eb4
keywords:
- Свойства DisplayName устаревшие функции среды Windows
- Свойства DisplayName устаревшие компоненты среды Windows, интерфейс Иресултверб
- Интерфейс Иресултверб устаревшие функции среды Windows, свойство DisplayName
topic_type:
- apiref
api_name:
- IResultVerb.DisplayName
- IResultVerb.get_DisplayName
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 721831274fc87ee65c8ee1655fdb7b38f80e1114
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071477"
---
# <a name="iresultverbdisplayname-property"></a>Иресултверб: свойство Исплайнаме:D

> [!NOTE]
> Windows Desktop Search 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003. В более поздних выпусках используйте [API поиска Windows](../search/-search-reference-entry-page.md) . 

Это свойство возвращает указатель на локализованное отображаемое имя для команды.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_DisplayName(
  [out, retval] BSTR *Verb
);
```



## <a name="property-value"></a>Значение свойства

Это свойство возвращает указатель на локализованное отображаемое имя для команды.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для настольных приложений Windows XP с пакетом обновления 2 \[\]<br/>                                      |
| Минимальная версия сервера<br/> | Только для настольных приложений Windows Server 2003 с пакетом обновления 1 \[\]<br/>                             |
| Распространяемые компоненты<br/>          | Windows Desktop Search (WDS) версии 2.6.5<br/>                                             |
| Header<br/>                   | <dl> <dt>Вдсшаредидл. h</dt> </dl> |



 

 





