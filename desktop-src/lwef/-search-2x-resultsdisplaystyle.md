---
title: Перечисление Ресултсдисплайстиле
description: Используется Иресултсвиевер Ресултсстиле для установки или определения способа отображения результатов.
ms.assetid: 24b474f2-1aca-4556-ba9a-3b8139e80bf0
keywords:
- Перечисление Ресултсдисплайстиле. устаревшие функции среды Windows
topic_type:
- apiref
api_name:
- ResultsDisplayStyle
api_location:
- WdsView.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26d564e0a7bb8a10b44e2957f26aa20a07afa535
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698976"
---
# <a name="resultsdisplaystyle-enumeration"></a>Перечисление Ресултсдисплайстиле

> [!NOTE]
> Windows Desktop Search 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003. В более поздних выпусках используйте [API поиска Windows](../search/-search-reference-entry-page.md) . 

Используется [**иресултсвиевер:: ресултсстиле**](-search-2x-iresultsviewer-resultsstyle.md) для задания или определения способа отображения результатов.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum ResultsDisplayStyleEnum { 
  SmallIconResults  = 0,
  LargeIconResults  = 1
} ResultsDisplayStyle;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="SmallIconResults"></span><span id="smalliconresults"></span><span id="SMALLICONRESULTS"></span>**смалликонресултс**
</dt> <dd>

Показывает, что результаты отображаются в виде мелких значков.

</dd> <dt>

<span id="LargeIconResults"></span><span id="largeiconresults"></span><span id="LARGEICONRESULTS"></span>**ларжеиконресултс**
</dt> <dd>

Показывает, что результаты отображаются в виде крупных значков.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|----------------------------------------------------------------------------------------|
| IDL<br/> | <dl> <dt>Вдсвиев. idl</dt> </dl> |



 

 





