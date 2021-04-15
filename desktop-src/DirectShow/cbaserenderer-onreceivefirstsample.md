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
ms.openlocfilehash: 2368b0e2abda3bcdd08872d730f8b9902dad43ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669409"
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

## <a name="remarks"></a>Комментарии

Метод [**кбасерендерер:: Receive**](cbaserenderer-receive.md) вызывает этот метод. Он не выполняет никаких действий в базовом классе, но производный класс может его переопределить. Этот метод предназначен в первую очередь для модулей подготовки видео. Когда модуль подготовки видео приостанавливается, он обычно отображает первый пример в виде изображения по-прежнему.

При поиске графа во время приостановки также вызывается этот метод.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ренбасе. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасерендерер**](cbaserenderer.md)
</dt> </dl>

 

 




