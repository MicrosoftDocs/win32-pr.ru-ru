---
description: 'Метод StopAt информирует ПИН-код, когда следует отказаться от доставки данных. Этот метод реализует метод Иамстреамконтрол:: StopAt.'
ms.assetid: cc9f0fdc-253b-4feb-95ce-56ebc575a49b
title: Метод Кбасестреамконтрол. StopAt (Стрмктл. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.StopAt
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8e6b794f5f05721f403d943252c2aabd48614519
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674796"
---
# <a name="cbasestreamcontrolstopat-method"></a>Кбасестреамконтрол. StopAt, метод

`StopAt`Метод информирует ПИН-код, когда следует отказаться от доставки данных. Этот метод реализует метод [**иамстреамконтрол:: StopAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT StopAt(
   const REFERENCE_TIME *ptStop = NULL,
         BOOL           bSendExtra = FALSE,
         DWORD          dwCookie = 0
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*птстоп* 
</dt> <dd>

Указатель на значение [**\_ времени ссылки**](reference-time.md) , указывающее, когда ПИН-код должен прекращать доставку данных.

</dd> <dt>

*бсендекстра* 
</dt> <dd>

Задает логическое значение, указывающее, следует ли отправить дополнительный пример после запланированного времени окончания. Если **значение — true**, ПИН-код отправляет один дополнительный пример.

</dd> <dt>

*двкукие* 
</dt> <dd>

Указывает значение для отправки вместе с уведомлением о запуске.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ ОК.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Стрмктл. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасестреамконтрол**](cbasestreamcontrol.md)
</dt> </dl>

 

 




