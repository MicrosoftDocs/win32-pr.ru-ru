---
description: Метод размещения \_ мессажедраин задает для окна получение сообщений окон, отправленных обработчику видео.
ms.assetid: b2d2d489-a66f-474a-b8bf-b019179f6f69
title: Метод CBaseControlWindow.put_MessageDrain (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_MessageDrain
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f03f944a6af6ac99de6000a2507178eea510c06a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657868"
---
# <a name="cbasecontrolwindowput_messagedrain-method"></a>Кбасеконтролвиндов. размещение \_ метода мессажедраин

`put_MessageDrain`Метод задает для окна получение сообщений окна, отправленных обработчику видео.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_MessageDrain(
   OAHWND Drain
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Остановка* 
</dt> <dd>

Окно для публикации сообщений.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** .

## <a name="remarks"></a>Комментарии

Сообщения, отправляемые в фильтр модуля подготовки отчетов, можно отправить в другое окно. Эта функция члена регистрирует окно для получения этих сообщений. В отличие от функции-члена [**\_ owner кбасеконтролвиндов::p UT**](cbasecontrolwindow-put-owner.md) , эта функция-член не делает окно видео дочерним для другого окна. Он особенно полезен для модулей подготовки видео в полноэкранном режиме, которые не могут быть дочерними окнами.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ктлутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасеконтролвиндов**](cbasecontrolwindow.md)
</dt> </dl>

 

 




