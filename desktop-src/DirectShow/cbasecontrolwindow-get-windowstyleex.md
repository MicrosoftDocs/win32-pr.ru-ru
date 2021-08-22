---
description: Метод Get \_ виндовстиликс извлекает расширенные стили окна.
ms.assetid: 72955958-bbda-4b8f-9c28-6d3f5eb56a82
title: Метод CBaseControlWindow.get_WindowStyleEx (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_WindowStyleEx
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 082b541c9f04122616f4f96548f1b1e58d940a6060fb4af1ac0fe51fa4887bb8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119331214"
---
# <a name="cbasecontrolwindowget_windowstyleex-method"></a>Кбасеконтролвиндов. Get \_ виндовстиликс, метод

`get_WindowStyleEx`Метод получает расширенные стили окна.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_WindowStyleEx(
   long *pWindowStyleEx
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пвиндовстиликс* 
</dt> <dd>

Указатель на расширенные стили окна.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** .

## <a name="remarks"></a>Remarks

Эта функция члена получает расширенные стили окна. Он вызывает функцию члена [**кбасеконтролвиндов::D ожетвиндовстиле**](cbasecontrolwindow-dogetwindowstyle.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ктлутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасеконтролвиндов**](cbasecontrolwindow.md)
</dt> </dl>

 

 




