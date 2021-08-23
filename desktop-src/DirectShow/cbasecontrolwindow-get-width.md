---
description: Метод Get \_ Width извлекает текущую ширину окна.
ms.assetid: 8c5fbb0b-da80-4cfe-9c52-8ed4d9e52888
title: Метод CBaseControlWindow.get_Width (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Width
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3dff6e2a0929963f06c14aa8899b2a1d6a268db8f87b5067d2ed65f90964c803
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119768244"
---
# <a name="cbasecontrolwindowget_width-method"></a>Кбасеконтролвиндов. Get, \_ метод Width

`get_Width`Метод получает текущую ширину окна.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_Width(
   long *pWidth
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пвидс* 
</dt> <dd>

Указатель на ширину окна в пикселях.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** .

## <a name="remarks"></a>Remarks

Окно располагается на рабочем столе. Это выражение выражается в пикселях на четыре координаты (слева, сверху, справа и снизу). Интерфейсы, автоматически создаваемые OLE, обычно выражают эту точку по левому краю, по верхнему краю, по ширине и высоте. Это соглашение, используемое в DirectShow. Все координаты выражаются в пикселях, и изменение любой координаты приведет к немедленному обновлению окна.

Установка координат Left или Top перемещает окно влево или вверх соответственно; Эти координаты не влияют на ширину и высоту окна. Аналогично, установка ширины и высоты не влияет на координаты левой и верхней точек.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ктлутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасеконтролвиндов**](cbasecontrolwindow.md)
</dt> </dl>

 

 




