---
title: Свойство SortOrderProperty IResultsViewer (WdsView.h)
description: Это свойство задает или возвращает порядок столбцов для сортировки результатов по.
ms.assetid: ea05f4df-4caf-404f-8890-a109ca88555c
keywords:
- свойства сортордерпроперти устаревшей среды Windows
- свойства сортордерпроперти устаревшей среды Windows, интерфейс иресултсвиевер
- интерфейс иресултсвиевер устаревшие функции среды Windows, свойство сортордерпроперти
topic_type:
- apiref
api_name:
- IResultsViewer.SortOrderProperty
- IResultsViewer.get_SortOrderProperty
- IResultsViewer.put_SortOrderProperty
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01680ac46592887cf4f321b771ff0e46039c775c4e9e9d8ed1edbc893ab45977
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829174"
---
# <a name="iresultsviewersortorderproperty-property"></a>Свойство Иресултсвиевер:: Сортордерпроперти

> [!NOTE]
> Windows настольный поиск 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003. в более поздних выпусках используйте вместо этого [API Windows поиска](../search/-search-reference-entry-page.md) . 

Это свойство задает или возвращает порядок столбцов для сортировки результатов по.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_SortOrderProperty(
  [in]          ColumnSortOrder order
);

HRESULT get_SortOrderProperty(
  [out, retval] ColumnSortOrder *order
);
```



## <a name="property-value"></a>Значение свойства

Задает свойство [**колумнсортордер**](/windows/win32/api/mmcobj/ne-mmcobj-_columnsortorder) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP с пакетом обновления 2 (SP2) \[ только классические приложения\]<br/>                                 |
| Минимальная версия сервера<br/> | Windows Только для настольных приложений сервера 2003 с пакетом обновления 1 \[\]<br/>                        |
| Распространяемые компоненты<br/>          | Windows Поиск на рабочем столе (WDS) 2.6.5<br/>                                        |
| Заголовок<br/>                   | <dl> <dt>Вдсвиев. h</dt> </dl> |



 

 





