---
description: Метод Жетделиверибуффер извлекает пример носителя, содержащий пустой буфер.
ms.assetid: 5a20c11b-50f8-443e-a4d5-6bcffde741d5
title: Кбасеаутпутпин. Жетделиверибуффер, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.GetDeliveryBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2d118e21ea67932529c41b35595619c6e03b907718708ba285aa2a6578177f7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117823613"
---
# <a name="cbaseoutputpingetdeliverybuffer-method"></a>Кбасеаутпутпин. Жетделиверибуффер, метод

`GetDeliveryBuffer`Метод получает пример носителя, который содержит пустой буфер.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT GetDeliveryBuffer(
   IMediaSample   **ppSample,
   REFERENCE_TIME *pStartTime,
   REFERENCE_TIME *pEndTime,
   DWORD          dwFlags
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппсампле* 
</dt> <dd>

Адрес переменной, которая получает указатель на интерфейс [**имедиасампле**](/windows/desktop/api/Strmif/nn-strmif-imediasample) буфера.

</dd> <dt>

*пстарттиме* 
</dt> <dd>

Указатель на время начала выборки или **значение NULL**.

</dd> <dt>

*пендтиме* 
</dt> <dd>

Указатель на время окончания выборки или **значение NULL**.

</dd> <dt>

*dwFlags* 
</dt> <dd>

Побитовое сочетание флагов, поддерживаемых интерфейсом [**имемаллокатор::/buffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** . Возможные значения включают перечисленные в следующей таблице.



| Код возврата                                                                                   | Описание                        |
|-----------------------------------------------------------------------------------------------|------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>          | Успешно.<br/>                |
| <dl> <dt>**\_интерфейс E**</dt> </dl> | Распределитель недоступен.<br/> |



 

## <a name="remarks"></a>Remarks

Этот метод вызывает метод **имемаллокатор::/buffer** для распределителя и передает параметры в этот метод.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>амфилтер. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасеаутпутпин**](cbaseoutputpin.md)
</dt> </dl>

 

 




