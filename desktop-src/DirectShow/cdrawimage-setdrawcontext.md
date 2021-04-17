---
description: Метод Сетдравконтекст задает контексты устройств, используемые для рисования.
ms.assetid: dd752970-99b3-42bb-95a5-8103cab276da
title: Кдравимаже. Сетдравконтекст, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.SetDrawContext
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1d329dd45d1a02afd2cbd0daf8d0da8390b0b395
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657146"
---
# <a name="cdrawimagesetdrawcontext-method"></a>Кдравимаже. Сетдравконтекст, метод

`SetDrawContext`Метод задает контексты устройств, используемые для рисования.

## <a name="syntax"></a>Синтаксис


```C++
void SetDrawContext();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Этот метод получает контексты окна и устройства памяти из объекта-владельца [**кбасевиндов**](cbasewindow.md) . Вызывайте этот метод после инициализации окна, но перед началом рисования.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Винутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кдравимаже**](cdrawimage.md)
</dt> </dl>

 

 




