---
description: Метод Сенднотифивиндов сообщает о вышестоящем фильтре обработчика окна видео.
ms.assetid: f46390b1-d03a-4520-8c1d-b3f870d3bb0b
title: Кбасерендерер. Сенднотифивиндов, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SendNotifyWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2b4956ad2b20040b0d22903d2ffaa2c7b460af9250fe057d106db545173d53a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118157501"
---
# <a name="cbaserenderersendnotifywindow-method"></a>Кбасерендерер. Сенднотифивиндов, метод

`SendNotifyWindow`Метод уведомляет вышестоящий фильтр обработчика окна видео.

## <a name="syntax"></a>Синтаксис


```C++
void SendNotifyWindow(
   IPin *pPin,
   HWND hwnd
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппин* 
</dt> <dd>

Указатель на интерфейс [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) выходного ПИН-кода вышестоящего фильтра.

</dd> <dt>

*HWND* 
</dt> <dd>

Указатель на окно видео или **значение NULL**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Если выходной ПИН-код вышестоящего фильтра поддерживает интерфейс [**имедиаевентсинк**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) , этот метод отправляет ему код события [**\_ \_ окна уведомления EC**](ec-notify-window.md) вместе с маркером окна.

Модули подготовки видео могут переопределять методы [**кбасерендерер:: комплетеконнект**](cbaserenderer-completeconnect.md) для вызова этого метода. Он предоставляет механизм для формирования вышестоящего фильтра маркера окна. В этом случае Переопределите метод [**кбасерендерер:: бреакконнект**](cbaserenderer-breakconnect.md) и вызовите `SendNotifyWindow` его с помощью маркера **null** .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ренбасе. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасерендерер**](cbaserenderer.md)
</dt> </dl>

 

 




