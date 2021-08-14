---
description: Метод Жетовнервиндов Извлекает маркер окна-владельца m \_ хвндовнер.
ms.assetid: fa576b42-b4a7-4374-8ba4-7d21e86d9d61
title: Кбасеконтролвиндов. Жетовнервиндов, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetOwnerWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0cdb3073d1dd8055986b905d6e8f50967a304e5f294b0ffcaeddcd50d8c0ee33
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119432514"
---
# <a name="cbasecontrolwindowgetownerwindow-method"></a>Кбасеконтролвиндов. Жетовнервиндов, метод

`GetOwnerWindow`Метод получает маркер окна-владельца, **m \_ хвндовнер**.

## <a name="syntax"></a>Синтаксис


```C++
HWND GetOwnerWindow();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает окно владельца.

## <a name="remarks"></a>Remarks

Извлекает окно-владелец без вызова метода интерфейса. Используйте эту функцию-член вместо [**кбасеконтролвиндов:: Get \_ owner**](cbasecontrolwindow-get-owner.md), если только вы не вызываете ее извне с помощью метода [**ивидеовиндов:: Get \_ owner**](/windows/desktop/api/Control/nf-control-ivideowindow-get_owner) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ктлутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасеконтролвиндов**](cbasecontrolwindow.md)
</dt> </dl>

 

 




