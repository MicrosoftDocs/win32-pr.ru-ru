---
title: Свойство подсказки Иресултпроперти (Вдсшаредидл. h)
description: Специальное значение, используемое для облегчения извлечения данных.
ms.assetid: fa888c5e-898e-4f48-b87e-2d0d078fd1fe
keywords:
- Свойство подсказки устаревшие функции среды Windows
- Свойство подсказки устаревшие функции среды Windows, интерфейс Иресултпроперти
- Устаревшие функции среды Windows интерфейса Иресултпроперти, свойство указания
topic_type:
- apiref
api_name:
- IResultProperty.Hint
- IResultProperty.get_Hint
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3edfed528ab6a6833cced99c113c33e7e2f859d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691798"
---
# <a name="iresultpropertyhint-property"></a>Иресултпроперти:: Указание свойства

> [!NOTE]
> Windows Desktop Search 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003. В более поздних выпусках используйте [API поиска Windows](../search/-search-reference-entry-page.md) . 

Специальное значение, используемое для облегчения извлечения данных.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_Hint(
  [out, retval] ling *hint
);
```



## <a name="property-value"></a>Значение свойства

Возвращает указатель на подсказку.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для настольных приложений Windows XP с пакетом обновления 2 \[\]<br/>                                      |
| Минимальная версия сервера<br/> | Только для настольных приложений Windows Server 2003 с пакетом обновления 1 \[\]<br/>                             |
| Распространяемые компоненты<br/>          | Windows Desktop Search (WDS) версии 2.6.5<br/>                                             |
| Header<br/>                   | <dl> <dt>Вдсшаредидл. h</dt> </dl> |



 

 





