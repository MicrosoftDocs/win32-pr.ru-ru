---
title: Перечисление Хеадердисплайстиле
description: Используется Иресултсвиевер Хеадерстиле для установки или возврата текущего стиля заголовка.
ms.assetid: 13ae6317-d990-4ccf-83b3-275caf953611
keywords:
- Перечисление Хеадердисплайстиле. устаревшие функции среды Windows
topic_type:
- apiref
api_name:
- HeaderDisplayStyle
api_location:
- WdsView.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc65b17fa61b799fc9ab8ea7cc1b01380a5843c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695012"
---
# <a name="headerdisplaystyle-enumeration"></a>Перечисление Хеадердисплайстиле

> [!NOTE]
> Windows Desktop Search 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003. В более поздних выпусках используйте [API поиска Windows](../search/-search-reference-entry-page.md) . 

Используется [**иресултсвиевер:: хеадерстиле**](-search-2x-iresultsviewer-headerstyle.md) для установки или возврата текущего стиля заголовка.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum HeaderDisplayStyleEnum { 
  FullHeader     = 0,
  CompactHeader  = 1,
  NoHeader       = 2
} HeaderDisplayStyle;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="FullHeader"></span><span id="fullheader"></span><span id="FULLHEADER"></span>**фуллхеадер**
</dt> <dd>

Указывает или задает использование полных заголовков.

</dd> <dt>

<span id="CompactHeader"></span><span id="compactheader"></span><span id="COMPACTHEADER"></span>**компаксеадер**
</dt> <dd>

Указывает или задает использование Compact Headers.

</dd> <dt>

<span id="NoHeader"></span><span id="noheader"></span><span id="NOHEADER"></span>**Заголовок**
</dt> <dd>

Указывает или задает использование без заголовков.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|----------------------------------------------------------------------------------------|
| IDL<br/> | <dl> <dt>Вдсвиев. idl</dt> </dl> |



 

 





