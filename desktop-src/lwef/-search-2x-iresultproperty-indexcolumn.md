---
title: Свойство Индексколумн Иресултпроперти (Вдсшаредидл. h)
description: Имя столбца свойств в индексе.
ms.assetid: a043be43-49ef-46e0-bfb6-01104288e9ef
keywords:
- свойства индексколумн устаревшей среды Windows
- свойства индексколумн устаревшей среды Windows, интерфейс иресултпроперти
- интерфейс иресултпроперти устаревшие функции среды Windows, свойство индексколумн
topic_type:
- apiref
api_name:
- IResultProperty.IndexColumn
- IResultProperty.get_IndexColumn
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3a78d91b9e823dbf8d3c7a2273247706f9ae2bb04c6f64d08f5555eb875023c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118754777"
---
# <a name="iresultpropertyindexcolumn-property"></a>Свойство Иресултпроперти:: Индексколумн

> [!NOTE]
> Windows настольный поиск 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003. в более поздних выпусках используйте вместо этого [API Windows поиска](../search/-search-reference-entry-page.md) . 

Имя столбца свойств в индексе.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_IndexColumn(
  [out, retval] BSTR *column
);
```



## <a name="property-value"></a>Значение свойства

Возвращает указатель на имя столбца в индексе.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP с пакетом обновления 2 (SP2) \[ только классические приложения\]<br/>                                      |
| Минимальная версия сервера<br/> | Windows Только для настольных приложений сервера 2003 с пакетом обновления 1 \[\]<br/>                             |
| Распространяемые компоненты<br/>          | Windows Поиск на рабочем столе (WDS) 2.6.5<br/>                                             |
| Header<br/>                   | <dl> <dt>Вдсшаредидл. h</dt> </dl> |



 

 





