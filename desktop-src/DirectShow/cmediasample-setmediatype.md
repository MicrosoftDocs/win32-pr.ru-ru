---
description: 'Метод Сетмедиатипе задает тип носителя для образца. Этот метод реализует метод Имедиасампле:: Сетмедиатипе.'
ms.assetid: 4423cc1e-d6e1-49e7-9cc1-1a1d71a3497b
title: Кмедиасампле. Сетмедиатипе, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e7059e0d9b2d91b6a938c67445f185a2c9be0daf5831c30b235918ab7820b1b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119832174"
---
# <a name="cmediasamplesetmediatype-method"></a>Кмедиасампле. Сетмедиатипе, метод

`SetMediaType`Метод задает тип носителя для образца. Этот метод реализует метод [**имедиасампле:: сетмедиатипе**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatype) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetMediaType(
   AM_MEDIA_TYPE *pMediaType
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пмедиатипе* 
</dt> <dd>

Указатель на структуру [**\_ \_ типа мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает одно из значений **HRESULT** , приведенных в следующей таблице.



| Код возврата                                                                                   | Описание                    |
|-----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>          | Success<br/>             |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Недостаточно памяти<br/> |



 

## <a name="remarks"></a>Remarks

Этот метод задает переменную члена [**кмедиасампле:: m \_ пмедиатипе**](cmediasample-m-pmediatype.md) , которая указывает тип мультимедиа, и переменную элемента [**кмедиасампле:: m \_ dwFlags**](cmediasample-m-dwflags.md) , которая указывает, изменился ли тип мультимедиа.

Этот метод создает копию \_ \_ структуры типа мультимедиа AM.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>амфилтер. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кмедиасампле**](cmediasample.md)
</dt> </dl>

 

 




