---
description: Метод Жетвиндовпоситион извлекает текущие координаты окна.
ms.assetid: a2f46a87-b2cd-450f-8d2b-0f8695432fda
title: Кбасеконтролвиндов. Жетвиндовпоситион, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetWindowPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6d576f065e807c2af47621d43940d7e48c54f36f0617d20590953a5e83ab2fc9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966734"
---
# <a name="cbasecontrolwindowgetwindowposition-method"></a>Кбасеконтролвиндов. Жетвиндовпоситион, метод

`GetWindowPosition`Метод получает текущие координаты окна.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetWindowPosition(
   long *pLeft,
   long *pTop,
   long *pWidth,
   long *pHeight
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*плефт* 
</dt> <dd>

Указатель на левую координату в экранных координатах.

</dd> <dt>

*птоп* 
</dt> <dd>

Указатель на верхнюю координату в экранных координатах.

</dd> <dt>

*пвидс* 
</dt> <dd>

Указатель на ширину окна в экранных координатах.

</dd> <dt>

*феигхт* 
</dt> <dd>

Указатель на высоту окна в экранных координатах.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ктлутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасеконтролвиндов**](cbasecontrolwindow.md)
</dt> </dl>

 

 




