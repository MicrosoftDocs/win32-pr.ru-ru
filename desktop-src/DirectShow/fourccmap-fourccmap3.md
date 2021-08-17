---
description: Метод-конструктор, который обеспечивает сопоставление между типами формата мультимедиа типа DWORD старого стиля и подтипами GUID. Этот метод использует параметр "пгуид".
ms.assetid: 4de6cb49-938e-42f8-8687-dc60a0f23e87
title: 'Конструктор Фаурккмап:: Фаурккмап (FourCC. h) — параметр пгуид'
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
ms.openlocfilehash: 2c674791418a7668d7c7597e951e9a89613b9c8150865ff123263e9d0ef9ded2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119330444"
---
# <a name="fourccmapfourccmap-constructor-fourcch---pguid-parameter"></a>Конструктор Фаурккмап:: Фаурккмап (FourCC. h) — параметр пгуид

Метод конструктора. Конструктор обеспечивает сопоставление между типами формата мультимедиа типа **DWORD** старого стиля и подтипами **GUID** .

## <a name="syntax"></a>Синтаксис


```C++
FOURCCMap(
   const GUID *pguid
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пгуид* 
</dt> <dd>

Указатель на глобальный уникальный идентификатор (**GUID**).

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

 

 




