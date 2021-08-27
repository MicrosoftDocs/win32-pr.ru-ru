---
title: Свойство FilterType Иресултсвиевер (Вдсвиев. h)
description: Это свойство задает или возвращает имя типа прецеивед, по которому будут фильтроваться результаты.
ms.assetid: 025955eb-3e44-4e26-8b5f-ae92eb4c8300
keywords:
- свойства FilterType устаревшей среды Windows
- свойства FilterType устаревшей среды Windows, интерфейс иресултсвиевер
- интерфейс иресултсвиевер устаревшие функции среды Windows, свойство FilterType
topic_type:
- apiref
api_name:
- IResultsViewer.FilterType
- IResultsViewer.get_FilterType
- IResultsViewer.put_FilterType
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8f4e71a469ad68431721d99343b43b28ea0f0a82b7e393f5c402b0d88735db4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118754310"
---
# <a name="iresultsviewerfiltertype-property"></a>Свойство Иресултсвиевер:: FilterType

> [!NOTE]
> Windows настольный поиск 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003. в более поздних выпусках используйте вместо этого [API Windows поиска](../search/-search-reference-entry-page.md) . 

Это свойство задает или возвращает имя типа прецеивед, по которому будут фильтроваться результаты.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_FilterType(
  [in]          BSTR name
);

HRESULT get_FilterType(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a>Значение свойства

Задает воспринимаемый тип, используемый для фильтрации результатов.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP с пакетом обновления 2 (SP2) \[ только классические приложения\]<br/>                                 |
| Минимальная версия сервера<br/> | Windows Только для настольных приложений сервера 2003 с пакетом обновления 1 \[\]<br/>                        |
| Распространяемые компоненты<br/>          | Windows Поиск на рабочем столе (WDS) 2.6.5<br/>                                        |
| Header<br/>                   | <dl> <dt>Вдсвиев. h</dt> </dl> |



 

 





