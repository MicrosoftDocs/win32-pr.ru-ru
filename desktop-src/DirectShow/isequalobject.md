---
description: Функция Исекуалобжект проверяет, находятся ли два интерфейса в одном объекте.
ms.assetid: 51325e05-5a7f-4a80-a12e-2e7dedc028e2
title: Функция Исекуалобжект (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsEqualObject
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e959d687d7d6b11dc6055daeda789e728d875d70
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685295"
---
# <a name="isequalobject-function"></a>Функция Исекуалобжект

`IsEqualObject`Функция проверяет, находятся ли два интерфейса на одном объекте.

## <a name="syntax"></a>Синтаксис


```C++
BOOL WINAPI IsEqualObject(
   IUnknown *pFirst,
   IUnknown *pSecond
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пфирст* 
</dt> <dd>

Указатель на один интерфейс.

</dd> <dt>

*псеконд* 
</dt> <dd>

Указатель на другой интерфейс.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если интерфейсы находятся в одном объекте, или **false** в противном случае.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Вксутил. h (включение Streams. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Различные вспомогательные функции](miscellaneous-helper-functions.md)
</dt> </dl>

 

 




