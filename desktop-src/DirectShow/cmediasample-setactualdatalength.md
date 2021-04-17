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
ms.openlocfilehash: 825b02f43195424f9ceb5ecd23c4dcf26727ef8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665271"
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



 

## <a name="remarks"></a>Комментарии

Этот метод задает переменную члена [**кмедиасампле:: m \_ лактуал**](cmediasample-m-lactual.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кмедиасампле**](cmediasample.md)
</dt> </dl>

 

 




