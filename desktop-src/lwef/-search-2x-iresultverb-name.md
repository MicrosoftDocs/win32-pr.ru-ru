---
title: Свойство имени Иресултверб (Вдсшаредидл. h)
description: Это свойство возвращает указатель на имя кононикал для команды, например Print, Open и т. д.
ms.assetid: e911ef1c-0ac9-4b70-a3af-c05e42bd1f0f
keywords:
- свойства имени устаревшие Windows функции среды
- свойство Name устаревшие Windows компоненты среды, интерфейс иресултверб
- интерфейс иресултверб устаревшие функции среды Windows, свойство Name
topic_type:
- apiref
api_name:
- IResultVerb.Name
- IResultVerb.get_Name
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e58377a9286a6e3fe4abb8d0a1d4ebf9e10bd3072295484ca32fb56d465a6f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976974"
---
# <a name="iresultverbname-property"></a>Свойство Иресултверб:: Name

> [!NOTE]
> Windows настольный поиск 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003. в более поздних выпусках используйте вместо этого [API Windows поиска](../search/-search-reference-entry-page.md) . 

Это свойство возвращает указатель на имя кононикал для команды, например Print, Open и т. д.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_Name(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a>Значение свойства

Name — это указатель на имя кононикал для команды.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP с пакетом обновления 2 (SP2) \[ только классические приложения\]<br/>                                      |
| Минимальная версия сервера<br/> | Windows Только для настольных приложений сервера 2003 с пакетом обновления 1 \[\]<br/>                             |
| Распространяемые компоненты<br/>          | Windows Поиск на рабочем столе (WDS) 2.6.5<br/>                                             |
| Заголовок<br/>                   | <dl> <dt>Вдсшаредидл. h</dt> </dl> |



 

 





