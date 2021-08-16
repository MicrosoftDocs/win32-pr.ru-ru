---
description: Метод-конструктор, который обеспечивает сопоставление между типами формата мультимедиа типа DWORD старого стиля и подтипами GUID. Этот метод не использует параметры.
ms.assetid: 2152803c-f45f-43b0-9207-4eaeddf5eeb6
title: 'Конструктор Фаурккмап:: Фаурккмап (FourCC. h) — нет параметров'
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
ms.openlocfilehash: d856589146103e599a1cf67d2090dd64af7107d1c221c46b9c93852f989ade9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015732"
---
# <a name="fourccmapfourccmap-constructor-fourcch---no-parameters"></a>Конструктор Фаурккмап:: Фаурккмап (FourCC. h) — нет параметров

Метод конструктора. Конструктор обеспечивает сопоставление между типами формата мультимедиа типа **DWORD** старого стиля и подтипами **GUID** .

## <a name="syntax"></a>Синтаксис


```C++
FOURCCMap();
```



## <a name="parameters"></a>Параметры

Этот конструктор не имеет параметров.

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

 

 




