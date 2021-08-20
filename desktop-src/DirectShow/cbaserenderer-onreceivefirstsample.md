---
description: Метод Онрецеивефирстсампле вызывается, когда фильтр получает выборку при приостановке.
ms.assetid: 5bd481bf-a62d-4d3c-b875-b94298d12730
title: Кбасерендерер. Онрецеивефирстсампле, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnReceiveFirstSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 882a356f47aa146ec8ba1b06d7af43235c8213334c0d82d0a241c590654bf2a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118157704"
---
# <a name="cbaserendereronreceivefirstsample-method"></a>Кбасерендерер. Онрецеивефирстсампле, метод

`OnReceiveFirstSample`Метод вызывается, когда фильтр получает выборку при приостановке.

## <a name="syntax"></a>Синтаксис


```C++
virtual void OnReceiveFirstSample(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пмедиасампле* 
</dt> <dd>

Указатель на интерфейс [**имедиасампле**](/windows/desktop/api/Strmif/nn-strmif-imediasample) образца.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Метод [**кбасерендерер:: Receive**](cbaserenderer-receive.md) вызывает этот метод. Он не выполняет никаких действий в базовом классе, но производный класс может его переопределить. Этот метод предназначен в первую очередь для модулей подготовки видео. Когда модуль подготовки видео приостанавливается, он обычно отображает первый пример в виде изображения по-прежнему.

При поиске графа во время приостановки также вызывается этот метод.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ренбасе. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасерендерер**](cbaserenderer.md)
</dt> </dl>

 

 




