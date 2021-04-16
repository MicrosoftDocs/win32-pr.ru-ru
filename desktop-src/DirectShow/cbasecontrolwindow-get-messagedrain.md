---
description: Метод Get \_ мессажедраин извлекает текущую стоку сообщений.
ms.assetid: d679e7f7-4628-479b-b722-843cdd91ffe6
title: Метод CBaseControlWindow.get_MessageDrain (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_MessageDrain
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: aaf51c3f4297f238e51bbe8677303730c04b89d3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657068"
---
# <a name="cbasecontrolwindowget_messagedrain-method"></a>Кбасеконтролвиндов. Get \_ мессажедраин, метод

`get_MessageDrain`Метод получает текущую стоку сообщений.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_MessageDrain(
   OAHWND *Drain
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Остановка* 
</dt> <dd>

Указатель на текущее окно, принимающее сообщения окна.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** .

## <a name="remarks"></a>Комментарии

Сообщения, отправляемые в фильтр модуля подготовки отчетов, можно отправить в другое окно. Окно, зарегистрированное для получения этих сообщений (с помощью функции-члена **кбасеконтролвиндов:: Get \_ мессажедраин** ), является текущим стоком сообщений.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ктлутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасеконтролвиндов**](cbasecontrolwindow.md)
</dt> </dl>

 

 




