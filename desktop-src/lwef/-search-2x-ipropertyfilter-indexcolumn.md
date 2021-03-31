---
title: Свойство Индексколумн Ипропертифилтер (Вдсшаредидл. h)
description: Имя индексируемого столбца свойства, по которому производится фильтрация.
ms.assetid: 18ce0c89-bdaa-4f83-bf03-c11b55a842f5
keywords:
- Свойства Индексколумн устаревшие функции среды Windows
- Свойства Индексколумн устаревшие функции среды Windows, интерфейс Ипропертифилтер
- Интерфейс Ипропертифилтер устаревшие функции среды Windows, свойство Индексколумн
topic_type:
- apiref
api_name:
- IPropertyFilter.IndexColumn
- IPropertyFilter.get_IndexColumn
- IPropertyFilter.put_IndexColumn
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1e55a59b4615f4b6c19dcb5f07d16394d2531f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071574"
---
# <a name="ipropertyfilterindexcolumn-property"></a>Свойство Ипропертифилтер:: Индексколумн

> [!NOTE]
> Windows Desktop Search 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003. В более поздних выпусках используйте [API поиска Windows](../search/-search-reference-entry-page.md) . 

Имя индексируемого столбца свойства, по которому производится фильтрация.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_IndexColumn(
  [in]          BSTR column
);

HRESULT get_IndexColumn(
  [out, retval] BSTR *column
);
```



## <a name="property-value"></a>Значение свойства

Задает свойство Column.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для настольных приложений Windows XP с пакетом обновления 2 \[\]<br/>                                      |
| Минимальная версия сервера<br/> | Только для настольных приложений Windows Server 2003 с пакетом обновления 1 \[\]<br/>                             |
| Распространяемые компоненты<br/>          | Windows Desktop Search (WDS) версии 2.6.5<br/>                                             |
| Header<br/>                   | <dl> <dt>Вдсшаредидл. h</dt> </dl> |



 

 





