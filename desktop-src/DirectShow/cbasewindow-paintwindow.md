---
description: Метод Паинтвиндов вызывает перерисовку окна.
ms.assetid: dce3d782-00e5-4176-9365-378d59d48ebc
title: Кбасевиндов. Паинтвиндов, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.PaintWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3b0932422f85cb31d587485976dfacbaa51e2bf7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657955"
---
# <a name="cbasewindowpaintwindow-method"></a>Кбасевиндов. Паинтвиндов, метод

`PaintWindow`Метод вызывает перерисовку окна.

## <a name="syntax"></a>Синтаксис


```C++
void PaintWindow(
   BOOL bErase
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*берасе* 
</dt> <dd>

Логическое значение, указывающее, удаляется ли фон. Если значение равно **true**, фон удаляется.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Этот метод создает сообщение WM \_ Paint путем непроверки всей клиентской области окна.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Винутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасевиндов**](cbasewindow.md)
</dt> </dl>

 

 




