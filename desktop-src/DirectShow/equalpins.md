---
description: Функция Екуалпинс проверяет, находятся ли два контакта на одном объекте.
ms.assetid: b6a92cb6-f4a9-4a14-831c-3b123e4692c0
title: Функция Екуалпинс (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EqualPins
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9fdf499b494f41a0acc5cc446bc92deade61c045
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685197"
---
# <a name="equalpins-function"></a>Функция Екуалпинс

Функция Екуалпинс проверяет, находятся ли два контакта на одном объекте.

## <a name="syntax"></a>Синтаксис


```C++
BOOL EqualPins(
   IUnknown *pPin1,
   IUnknown *pPin2
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pPin1* 
</dt> <dd>

Указатель на один ПИН-код.

</dd> <dt>

*pPin2* 
</dt> <dd>

Указатель на другой ПИН-код.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если оба контакта находятся в одном объекте, или **false** в противном случае.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Вксутил. h (включение Streams. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Различные вспомогательные функции](miscellaneous-helper-functions.md)
</dt> </dl>

 

 




