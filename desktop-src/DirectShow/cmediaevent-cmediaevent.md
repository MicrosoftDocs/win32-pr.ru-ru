---
description: Метод конструктора Кмедиаевент. Кмедиаевент.
ms.assetid: 7f7a0a9f-e531-4e22-8601-b84ab088e9e7
title: Конструктор Кмедиаевент. Кмедиаевент (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaEvent.CMediaEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 36cd82b086241012542701001c4de1fe16ac2d8e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095562"
---
# <a name="cmediaeventcmediaevent-constructor"></a>Кмедиаевент. Кмедиаевент, конструктор

Метод конструктора.

## <a name="syntax"></a>Синтаксис


```C++
CMediaEvent(
   const TCHAR     *pName,
         LPUNKNOWN pUnk
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pName* 
</dt> <dd>

Указатель на имя объекта для целей отладки.

</dd> <dt>

*pUnk* 
</dt> <dd>

Указатель на владельца этого объекта.

</dd> </dl>

## <a name="remarks"></a>Remarks

Выделите параметр *pName* в статической памяти. Это имя отображается в терминале отладки при создании и удалении объекта.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ктлутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кмедиаевент**](cmediaevent.md)
</dt> </dl>

 

 




