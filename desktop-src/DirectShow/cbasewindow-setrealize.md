---
description: Метод Сетреализе указывает, реализует ли окно палитры.
ms.assetid: ab4a6069-c11f-4126-93bf-6de5277970a1
title: Кбасевиндов. Сетреализе, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.SetRealize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 825a020b73bc74b38a32daa6f6870b76a009f5b8090e253370c77dfce7d7dc31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954572"
---
# <a name="cbasewindowsetrealize-method"></a>Кбасевиндов. Сетреализе, метод

`SetRealize`Метод указывает, реализует ли окно палитры.

## <a name="syntax"></a>Синтаксис


```C++
void SetRealize(
   BOOL bRealize
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*бреализе* 
</dt> <dd>

Логическое значение, указывающее, следует ли реализовывать палитры. Если **значение равно true**, метод [**Кбасевиндов:: сетпалетте**](cbasewindow-setpalette.md) реализует палитры.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

По умолчанию метод **сетпалетте** реализует указанную палитру. Вызовите этот метод, чтобы изменить поведение по умолчанию, чтобы палитры были выбраны, но не были реализованы. Этот метод задает переменную члена [**кбасевиндов:: m \_ бнореализе**](cbasewindow-m-bnorealize.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>винутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасевиндов**](cbasewindow.md)
</dt> </dl>

 

 




