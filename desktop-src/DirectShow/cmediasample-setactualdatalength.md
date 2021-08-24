---
description: 'Метод Сетактуалдаталенгс задает длину допустимых данных в буфере. Этот метод реализует метод Имедиасампле:: Сетактуалдаталенгс.'
ms.assetid: a80a67ef-e490-4874-a123-f2d193cec4d7
title: Кмедиасампле. Сетактуалдаталенгс, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetActualDataLength
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: db090ad96f6c53f725aef7864e729b8083bfd1a02b30f0d699d30b5c6f8f71aa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634383"
---
# <a name="cmediasamplesetactualdatalength-method"></a>Кмедиасампле. Сетактуалдаталенгс, метод

`SetActualDataLength`Метод задает длину допустимых данных в буфере. Этот метод реализует метод [**имедиасампле:: сетактуалдаталенгс**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setactualdatalength) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetActualDataLength(
   long lLen
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ллен* 
</dt> <dd>

Длина допустимых данных в байтах.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает одно из значений **HRESULT** , приведенных в следующей таблице.



| Код возврата                                                                                             | Описание                                                 |
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>                    | Успешно.<br/>                                         |
| <dl> <dt>**\_ \_ переполнение буфера VFW E \_**</dt> </dl> | *ллен* больше размера выделенного буфера.<br/> |



 

## <a name="remarks"></a>Remarks

Этот метод задает переменную члена [**кмедиасампле:: m \_ лактуал**](cmediasample-m-lactual.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>амфилтер. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кмедиасампле**](cmediasample.md)
</dt> </dl>

 

 




