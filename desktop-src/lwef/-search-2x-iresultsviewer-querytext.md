---
title: Свойство QueryText Иресултсвиевер (Вдсвиев. h)
description: Возвращает или задает текст текущего запроса.
ms.assetid: 3d6b31fa-3f17-45de-a91a-f24a6b076099
keywords:
- свойства QueryText устаревшей среды Windows
- свойства QueryText устаревшей среды Windows, интерфейс иресултсвиевер
- интерфейс иресултсвиевер устаревшие функции среды Windows, свойство QueryText
topic_type:
- apiref
api_name:
- IResultsViewer.QueryText
- IResultsViewer.get_QueryText
- IResultsViewer.put_QueryText
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5522419d14bf27a1e836c9caa16e9dabf5a122e4566fd19c868a1f72e3f61d73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118753589"
---
# <a name="iresultsviewerquerytext-property"></a>Свойство Иресултсвиевер:: QueryText

> [!NOTE]
> Windows настольный поиск 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003. в более поздних выпусках используйте вместо этого [API Windows поиска](../search/-search-reference-entry-page.md) . 

Возвращает или задает текст текущего запроса.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_QueryText(
  [in]          BSTR query
);

HRESULT get_QueryText(
  [out, retval] BSTR *query
);
```



## <a name="property-value"></a>Значение свойства

Задает текст текущего запроса.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP с пакетом обновления 2 (SP2) \[ только классические приложения\]<br/>                                 |
| Минимальная версия сервера<br/> | Windows Только для настольных приложений сервера 2003 с пакетом обновления 1 \[\]<br/>                        |
| Распространяемые компоненты<br/>          | Windows Поиск на рабочем столе (WDS) 2.6.5<br/>                                        |
| Header<br/>                   | <dl> <dt>Вдсвиев. h</dt> </dl> |



 

 





