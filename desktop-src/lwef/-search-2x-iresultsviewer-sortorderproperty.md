---
title: Свойство SortOrderProperty IResultsViewer (WdsView.h)
description: Это свойство задает или возвращает порядок столбцов для сортировки результатов по.
ms.assetid: ea05f4df-4caf-404f-8890-a109ca88555c
keywords:
- Свойства Сортордерпроперти устаревшие функции среды Windows
- Свойства Сортордерпроперти устаревшие функции среды Windows, интерфейс Иресултсвиевер
- Интерфейс Иресултсвиевер устаревшие функции среды Windows, свойство Сортордерпроперти
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
ms.openlocfilehash: 2fa36dba99afbee58b480e17f241cb32f75cd5dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672649"
---
# <a name="iresultsviewersortorderproperty-property"></a>Свойство Иресултсвиевер:: Сортордерпроперти

> [!NOTE]
> Windows Desktop Search 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003. В более поздних выпусках используйте [API поиска Windows](../search/-search-reference-entry-page.md) . 

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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для настольных приложений Windows XP с пакетом обновления 2 \[\]<br/>                                 |
| Минимальная версия сервера<br/> | Только для настольных приложений Windows Server 2003 с пакетом обновления 1 \[\]<br/>                        |
| Распространяемые компоненты<br/>          | Windows Desktop Search (WDS) версии 2.6.5<br/>                                        |
| Header<br/>                   | <dl> <dt>Вдсвиев. h</dt> </dl> |



 

 





