---
title: Свойство ItemStore Иресултсвиевер (Вдсвиев. h)
description: Это свойство задает или возвращает имя хранилища, по которому будут фильтроваться результаты.
ms.assetid: c2a60485-c8f7-4951-a75e-2e6f6dcc2e4f
keywords:
- свойства ItemStore устаревшей среды Windows
- свойства ItemStore устаревшей среды Windows, интерфейс иресултсвиевер
- интерфейс иресултсвиевер устаревшие функции среды Windows, свойство ItemStore
topic_type:
- apiref
api_name:
- IResultsViewer.ItemStore
- IResultsViewer.get_ItemStore
- IResultsViewer.put_ItemStore
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b21db485f8bfeb52ac413a2886f5624345e9812f2a0086b143f9a10942f7aa74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118753905"
---
# <a name="iresultsvieweritemstore-property"></a>Свойство Иресултсвиевер:: ItemStore

> [!NOTE]
> Windows настольный поиск 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003. в более поздних выпусках используйте вместо этого [API Windows поиска](../search/-search-reference-entry-page.md) . 

Это свойство задает или возвращает имя хранилища, по которому будут фильтроваться результаты.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_ItemStore(
  [in]          BSTR name
);

HRESULT get_ItemStore(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a>Значение свойства

Задает имена хранилища.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP с пакетом обновления 2 (SP2) \[ только классические приложения\]<br/>                                 |
| Минимальная версия сервера<br/> | Windows Только для настольных приложений сервера 2003 с пакетом обновления 1 \[\]<br/>                        |
| Распространяемые компоненты<br/>          | Windows Поиск на рабочем столе (WDS) 2.6.5<br/>                                        |
| Header<br/>                   | <dl> <dt>Вдсвиев. h</dt> </dl> |



 

 





