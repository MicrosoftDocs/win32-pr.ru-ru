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
ms.openlocfilehash: 9cfd9cbb93a4d517391be0afe591d3378d9ecef32a0013ab452d31b9eecb6d59
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043214"
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

## <a name="remarks"></a>Remarks

Если этот объект создан с помощью кода **FourCC** , для его сопоставления создается **идентификатор GUID** . Если этот объект создается с существующим **идентификатором GUID**, значение **FourCC** объекта устанавливается в 0. Впоследствии значение **FourCC** можно задать или получить с помощью функций члена [**сетфауркк**](fourccmap-setfourcc.md) и [**жетфауркк**](fourccmap-getfourcc.md) соответственно.

## <a name="requirements"></a>Требования

| Требование | Значение |
|-|-|
| Заголовок  | Fourcc. h (включает Потоки. h) |
| Библиотека | Стрмбасе. lib (розничные сборки); Стрмбасд. lib (отладочные сборки) |

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Фаурккмап**](fourccmap.md)
</dt> </dl>

 

 




