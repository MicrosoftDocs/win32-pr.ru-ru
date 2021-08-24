---
title: Перечисление Ресултсдисплайстиле
description: Используется Иресултсвиевер Ресултсстиле для установки или определения способа отображения результатов.
ms.assetid: 24b474f2-1aca-4556-ba9a-3b8139e80bf0
keywords:
- ресултсдисплайстиле перечисления устаревших компонентов среды Windows
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
ms.openlocfilehash: 97a045765b53f29e978c286a14a1d82b86ffb21b5046dee606029a957ee0434c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726533"
---
# <a name="resultsdisplaystyle-enumeration"></a>Перечисление Ресултсдисплайстиле

> [!NOTE]
> Windows настольный поиск 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003. в более поздних выпусках используйте вместо этого [API Windows поиска](../search/-search-reference-entry-page.md) . 

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



 

 





