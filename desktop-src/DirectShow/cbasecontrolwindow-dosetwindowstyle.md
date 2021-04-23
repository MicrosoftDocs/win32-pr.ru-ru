---
description: Метод Досетвиндовстиле изменяет стандартные или расширенные стили окна.
ms.assetid: 4a9a97fb-b527-44ce-af8c-e5ea832ed4c4
title: Кбасеконтролвиндов. Досетвиндовстиле, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.DoSetWindowStyle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: db88c5818d31d65f361ae1a805bd50c285d4a5c2
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909812"
---
# <a name="cbasecontrolwindowdosetwindowstyle-method"></a>Кбасеконтролвиндов. Досетвиндовстиле, метод

`DoSetWindowStyle`Метод изменяет стандартные или расширенные стили окна.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT DoSetWindowStyle(
   long Style,
   long WindowLong
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Стиль* 
</dt> <dd>

Соответствующие стили окна.

</dd> <dt>

*виндовлонг* 
</dt> <dd>

Значение, указывающее, какие стили задаются. Должна быть одной из следующих:



| Метка | Значение |
|--------------|--------------------------------------|
| \_стиль ГВЛ   | Получение стилей окна.          |
| ГВЛ \_ операторе EXSTYLE | Получение расширенных стилей окна. |



 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** .

## <a name="remarks"></a>Комментарии

Эта функция члена вызывает функцию Win32 **SetWindowLong** для задания стиля окна, а затем повторно отображает окно в текущей позицией. Эта функция-член вызывается с помощью функций-членов [**кбасеконтролвиндов::p UT \_ WindowStyle**](cbasecontrolwindow-put-windowstyle.md) и [**кбасеконтролвиндов::p UT \_ виндовстиликс**](cbasecontrolwindow-put-windowstyleex.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Ктлутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасеконтролвиндов**](cbasecontrolwindow.md)
</dt> </dl>

 

 




