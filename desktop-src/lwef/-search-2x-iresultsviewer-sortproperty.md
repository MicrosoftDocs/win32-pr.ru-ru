---
title: Свойство SortProperty Иресултсвиевер (Вдсвиев. h)
description: Это свойство задаст или возвратит Индексколумн свойства для сортировки результатов по.
ms.assetid: 5b117f2e-52cc-43ef-9ebd-d7a800015465
keywords:
- Свойства SortProperty устаревшие функции среды Windows
- Свойства SortProperty устаревшие функции среды Windows, интерфейс Иресултсвиевер
- Интерфейс Иресултсвиевер устаревшие функции среды Windows, свойство SortProperty
topic_type:
- apiref
api_name:
- IResultsViewer.SortProperty
- IResultsViewer.get_SortProperty
- IResultsViewer.put_SortProperty
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cb75b98f1f0a726ef0d61b5c476df1485ba7189
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891857"
---
# <a name="iresultsviewersortproperty-property"></a>Свойство Иресултсвиевер:: SortProperty

> [!NOTE]
> Windows Desktop Search 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003. В более поздних выпусках используйте [API поиска Windows](../search/-search-reference-entry-page.md) . 

Это свойство задаст или возвратит Индексколумн свойства для сортировки результатов по.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_SortProperty(
  [in]          BSTR column
);

HRESULT get_SortProperty(
  [out, retval] BSTR *column
);
```



## <a name="property-value"></a>Значение свойства

Задает свойство Индексколумн.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для настольных приложений Windows XP с пакетом обновления 2 \[\]<br/>                                 |
| Минимальная версия сервера<br/> | Только для настольных приложений Windows Server 2003 с пакетом обновления 1 \[\]<br/>                        |
| Распространяемые компоненты<br/>          | Windows Desktop Search (WDS) версии 2.6.5<br/>                                        |
| Header<br/>                   | <dl> <dt>Вдсвиев. h</dt> </dl> |



 

 





