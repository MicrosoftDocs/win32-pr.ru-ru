---
description: Метод Поссиблеатмессаже позволяет производному классу пересылать сообщения в другое окно.
ms.assetid: d8775182-44ed-4df2-b4b8-1fdf289e2c1a
title: Кбасевиндов. Поссиблеатмессаже, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.PossiblyEatMessage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 851f46d14f949a49c9422256f9b2bda1ba314e5789773121387e89c011f7a424
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016462"
---
# <a name="cbasewindowpossiblyeatmessage-method"></a>Кбасевиндов. Поссиблеатмессаже, метод

`PossiblyEatMessage`Метод позволяет производному классу пересылать сообщения в другое окно.

## <a name="syntax"></a>Синтаксис


```C++
virtual BOOL PossiblyEatMessage(
   UINT   uMsg,
   WPARAM wParam,
   LPARAM lParam
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Uiacp* 
</dt> <dd>

Идентификатор сообщения.

</dd> <dt>

*wParam* 
</dt> <dd>

Первый параметр сообщения.

</dd> <dt>

*lParam* 
</dt> <dd>

Второй параметр сообщения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если сообщение было переслано, или **значение false** в противном случае. Базовый класс возвращает **значение false**.

## <a name="remarks"></a>Remarks

Перед тем как метод [**кбасевиндов:: онрецеивемессаже**](cbasewindow-onreceivemessage.md) обрабатывает сообщение, он вызывает `PossiblyEatMessage` . Если `PossiblyEatMessage` возвращает **значение true**, **онрецеивемессаже** игнорирует сообщение. Производный класс может переопределить `PossiblyEatMessage` , чтобы он перенаправлял некоторые сообщения в окно владельца. Например, класс [**кбасеконтролвиндов**](cbasecontrolwindow.md) , который является производным от **кбасевиндов**, перенаправляет сообщения клавиатуры и мыши.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>винутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасевиндов**](cbasewindow.md)
</dt> </dl>

 

 




