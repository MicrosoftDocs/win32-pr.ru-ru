---
description: Метод Рекордфрамелатенесс записывает, как своевременно выполнялась визуализация, и собирает статистику для страницы свойств.
ms.assetid: 9d4b90d7-b529-40cc-a0fd-6635163fb7dd
title: Кбасевидеорендерер. Рекордфрамелатенесс, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.RecordFrameLateness
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 10ae7069ceedbe43f9614ea3fd1c7c901d7023cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675007"
---
# <a name="cbasevideorendererrecordframelateness-method"></a>Кбасевидеорендерер. Рекордфрамелатенесс, метод

`RecordFrameLateness`Метод записывает, как своевременно выполнялась визуализация, и собирает статистику для страницы свойств.

## <a name="syntax"></a>Синтаксис


```C++
virtual void RecordFrameLateness(
   int trLate,
   int trFrame
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*трлате* 
</dt> <dd>

Значение, указывающее, насколько поздно образец превысил время его выполнения в ссылочных единицах времени.

</dd> <dt>

*трфраме* 
</dt> <dd>

Время между кадрами, в ссылочных единицах времени.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ренбасе. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасевидеорендерер**](cbasevideorenderer.md)
</dt> </dl>

 

 




