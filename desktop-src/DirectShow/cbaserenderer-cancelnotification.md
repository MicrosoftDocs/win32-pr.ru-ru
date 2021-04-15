---
description: Метод Канцелнотификатион отменяет событие таймера, которое планирует подготовку к просмотру.
ms.assetid: 56ddf692-a2e3-40f2-848f-2d592601ec00
title: Кбасерендерер. Канцелнотификатион, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CancelNotification
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3330f369c5fcc45fe051a1964a504d5d40fcd091
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668749"
---
# <a name="cbaserenderercancelnotification-method"></a>Кбасерендерер. Канцелнотификатион, метод

`CancelNotification`Метод отменяет событие таймера, которое планирует подготовку к просмотру.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT CancelNotification();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает одно из значений **HRESULT** , приведенных в следующей таблице.



| Код возврата                                                                             | Описание                                  |
|-----------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Нет ожидающего события таймера.<br/> |
| <dl> <dt>**\_ОК**</dt> </dl>    | Успешно.<br/>                          |



 

## <a name="remarks"></a>Комментарии

Фильтр вызывает этот метод при остановке потоковой передачи. Метод отменяет любую запланированную отрисовку.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ренбасе. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасерендерер**](cbaserenderer.md)
</dt> </dl>

 

 




