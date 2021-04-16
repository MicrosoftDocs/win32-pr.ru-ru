---
description: Метод-конструктор, который обеспечивает сопоставление между типами формата мультимедиа типа DWORD старого стиля и подтипами GUID. Этот метод использует параметр "FourCC".
ms.assetid: 35344aae-ed87-4e5e-8824-84f5482b332e
title: 'Конструктор Фаурккмап:: Фаурккмап (FourCC. h) — параметр FourCC'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FOURCCMap.FOURCCMap
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cbcd5e8a7c37d3265f508ac7632ffd4b18c8a00f
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/19/2021
ms.locfileid: "105651564"
---
# <a name="fourccmapfourccmap-constructor-fourcch---fourcc-parameter"></a>Конструктор Фаурккмап:: Фаурккмап (FourCC. h) — параметр FourCC

Метод конструктора. Конструктор обеспечивает сопоставление между типами формата мультимедиа типа **DWORD** старого стиля и подтипами **GUID** .

## <a name="syntax"></a>Синтаксис


```C++
FOURCCMap(
   DWORD Fourcc
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*FourCC* 
</dt> <dd>

**Параметр DWORD** , указывающий FourCC.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Если этот объект создан с помощью кода **FourCC** , для его сопоставления создается **идентификатор GUID** . Если этот объект создается с существующим **идентификатором GUID**, значение **FourCC** объекта устанавливается в 0. Впоследствии значение **FourCC** можно задать или получить с помощью функций члена [**сетфауркк**](fourccmap-setfourcc.md) и [**жетфауркк**](fourccmap-getfourcc.md) соответственно.

## <a name="requirements"></a>Требования

| Требование | Значение |
|-|-|
| Header  | FourCC. h (включение Streams. h) |
| Библиотека | Стрмбасе. lib (розничные сборки); Стрмбасд. lib (отладочные сборки) |

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Фаурккмап**](fourccmap.md)
</dt> </dl>

 

 




