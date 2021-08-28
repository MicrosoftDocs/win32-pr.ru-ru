---
description: Метод размещения \_ Left задает левую координату для окна.
ms.assetid: 4ba6b243-e7a7-4c41-a2c5-248b05b42f4f
title: Метод CBaseControlWindow.put_Left (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Left
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 70d0e582e358f988ea1ecd72cac0b9c62a88eaed474a413c47331b59b9fb1126
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793724"
---
# <a name="cbasecontrolwindowput_left-method"></a>Кбасеконтролвиндов. размещение \_ Left, метод

`put_Left`Метод задает левую координату окна.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_Left(
   long Left
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Слева* 
</dt> <dd>

Новая левая координата (в пикселях).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** .

## <a name="remarks"></a>Remarks

Окно располагается на рабочем столе. Это выражение выражается в пикселях на четыре координаты (слева, сверху, справа и снизу). Интерфейсы, автоматически создаваемые OLE, обычно выражают эту точку по левому краю, по верхнему краю, по ширине и высоте. Это соглашение, используемое в DirectShow. Все координаты выражаются в пикселях, и изменение любой координаты приведет к немедленному обновлению окна.

Установка координат Left или Top перемещает окно влево или вверх соответственно; Эти координаты не влияют на ширину и высоту окна. Аналогично, установка ширины и высоты не влияет на координаты левой и верхней точек.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ктлутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасеконтролвиндов**](cbasecontrolwindow.md)
</dt> </dl>

 

 




