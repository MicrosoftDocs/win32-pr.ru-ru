---
title: Свойство DisplayName Иресултсвиевер (Вдсвиев. h)
description: Локализованное отображаемое имя типа.
ms.assetid: 22503996-e693-47bc-b84f-cc4d3af2cb78
keywords:
- функции свойства DisplayName прежних версий Windows
- свойства DisplayName прежних версий Windows функции среды, интерфейс иресултсвиевер
- интерфейс иресултсвиевер устаревшие функции среды Windows, свойство DisplayName
topic_type:
- apiref
api_name:
- IResultsViewer.DisplayName
- IResultsViewer.get_DisplayName
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98d3f0c5f7887861d2d757c71a4327ce57af7f39ae3f4811167789c6b4e662ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118754399"
---
# <a name="iresultsviewerdisplayname-property"></a>Иресултсвиевер: свойство Исплайнаме:D

> [!NOTE]
> Windows настольный поиск 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003. в более поздних выпусках используйте вместо этого [API Windows поиска](../search/-search-reference-entry-page.md) . 

Локализованное отображаемое имя типа.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_DisplayName(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a>Значение свойства

Указатель на значение, получающее локализованное отображаемое имя для типа.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP с пакетом обновления 2 (SP2) \[ только классические приложения\]<br/>                                 |
| Минимальная версия сервера<br/> | Windows Только для настольных приложений сервера 2003 с пакетом обновления 1 \[\]<br/>                        |
| Распространяемые компоненты<br/>          | Windows Поиск на рабочем столе (WDS) 2.6.5<br/>                                        |
| Заголовок<br/>                   | <dl> <dt>Вдсвиев. h</dt> </dl> |



 

 





