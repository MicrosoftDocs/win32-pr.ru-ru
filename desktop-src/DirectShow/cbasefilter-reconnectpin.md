---
description: Метод Реконнектпин прерывает существующее подключение к заданному ПИН-коду и повторно подключает его к тому же ПИН-коду, используя указанный тип носителя.
ms.assetid: 9e2dea49-a2bd-4abd-b896-54b13b2271bb
title: Кбасефилтер. Реконнектпин, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.ReconnectPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 22507995621d708e40437175d7004d10f68fedb5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105656870"
---
# <a name="cbasefilterreconnectpin-method"></a>Кбасефилтер. Реконнектпин, метод

`ReconnectPin`Метод прерывает существующее подключение к заданному ПИН-коду и повторно подключает его к тому же ПИН-коду, используя указанный тип носителя.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ReconnectPin(
   IPin                *pPin,
   AM_MEDIA_TYPE const *pmt
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппин* 
</dt> <dd>

Указатель на интерфейс [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) ПИН-кода.

</dd> <dt>

*состоит* 
</dt> <dd>

Указатель на структуру [**\_ \_ типа файлов мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) , указывающую тип носителя, или **значение NULL**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** . Возможные значения включают перечисленные в следующей таблице.



| Код возврата                                                                                   | Описание                                                                       |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>          | Успешно.<br/>                                                               |
| <dl> <dt>**\_интерфейс E**</dt> </dl> | Переменная-член [**m \_ Пграф**](cbasefilter-m-pgraph.md) имеет **значение NULL**.<br/> |



 

## <a name="remarks"></a>Комментарии

Этот метод вызывает метод [**IFilterGraph2:: реконнектекс**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-reconnectex) в диспетчере графов фильтров. Если интерфейс [**IFilterGraph2**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph2) недоступен, метод вызывает [**ифилтерграф:: Reconnect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-reconnect).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасефилтер**](cbasefilter.md)
</dt> </dl>

 

 




