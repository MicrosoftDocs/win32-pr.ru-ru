---
description: 'Ктрансформаутпутпин. notify, метод notify уведомляет ПИН-код о том, что запрошено изменение качества. Этот метод реализует метод Икуалитиконтрол:: notify.'
ms.assetid: cdb93eef-90d5-4111-a3d4-175903f44a13
title: Метод Ктрансформаутпутпин. notify (Трансфрм. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.Notify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9a55e493c737b5a5864ec0a8dd38eee3abbfa586
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084812"
---
# <a name="ctransformoutputpinnotify-method"></a>Ктрансформаутпутпин. notify, метод

`Notify`Метод уведомляет ПИН-код о том, что запрошено изменение качества. Этот метод реализует метод [**икуалитиконтрол:: notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Notify(
   IBaseFilter *pSelf,
   Quality     q
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пселф* 
</dt> <dd>

Указатель на интерфейс [**ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) фильтра, который доставил сообщение контроля качества.

</dd> <dt>

*формате* 
</dt> <dd>

Структура [**качества**](/windows/win32/api/strmif/ns-strmif-quality) , содержащая сообщение контроля качества.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** . Возможные значения включают в себя, показанные в следующей таблице.



| Код возврата                                                                                       | Описание                                                |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>              | Успешно.<br/>                                        |
| <dl> <dt>**VFW \_ E \_ не \_ найден**</dt> </dl> | Не удалось найти объект для приема сообщения.<br/> |



 

## <a name="remarks"></a>Remarks

Этот метод вызывает метод [**ктрансформфилтер:: алтеркуалити**](ctransformfilter-alterquality.md) фильтра. Если фильтр не обрабатывает сообщение качества, этот метод вызывает метод [**кбасеинпутпин::P асснотифи**](cbaseinputpin-passnotify.md) для входного ПИН-кода фильтра. Метод **пасснотифи** передает исходящий текст сообщения (или в пользовательский диспетчер качества, если он был установлен).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Трансфрм. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



 

 




